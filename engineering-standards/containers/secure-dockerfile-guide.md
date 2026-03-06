# 🐳 Secure Containerization & Dockerfile Standards

Containerization is the backbone of modern microservices, but a poorly written Dockerfile is a significant security risk. I follow strict containerization standards to ensure your applications are **secure, fast, and lightweight.**

---

## 🛠️ My Container Best Practices

Every Dockerfile I write for your project will adhere to the following standards:

### 1. Multi-Stage Builds
*   **Why:** To separate the build environment (compilers, source code, dev dependencies) from the runtime environment.
*   **Result:** A significantly smaller production image (e.g., reducing a 1GB image to 50MB) and a massive reduction in the attack surface.

### 2. Running as Non-Root
*   **Why:** To prevent container breakout attacks. If an attacker gains entry, they are limited by the permissions of the non-root user.
*   **Method:** I explicitly create a user and group, then switch to it using `USER appuser`.

### 3. Minimal Base Images
*   **Why:** Standard OS images (like Ubuntu or Debian) include hundreds of packages that aren't needed, all of which could have vulnerabilities.
*   **My Choice:** I prefer **Alpine Linux** (minimalist) or **Distroless** (no shell, no package manager) for production workloads.

### 4. No Secrets in Layers
*   **Why:** Environment variables or build arguments can be cached in image layers, potentially exposing sensitive keys.
*   **Method:** Secrets are passed at runtime via orchestration tools (e.g., Kubernetes Secrets, AWS ECS Secrets) rather than being baked into the image.

---

## 📄 Example: Secure Multi-Stage Dockerfile (Node.js)

```dockerfile
# Stage 1: Build
FROM node:18-alpine AS builder
WORKDIR /app
COPY package*.json ./
RUN npm ci
COPY . .
RUN npm run build

# Stage 2: Runtime
FROM node:18-alpine
# Create non-root user
RUN addgroup -S appgroup && adduser -S appuser -G appgroup
WORKDIR /app
# Only copy production artifacts
COPY --from=builder /app/dist ./dist
COPY --from=builder /app/package*.json ./
RUN npm ci --only=production

USER appuser
EXPOSE 3000
CMD ["node", "dist/main.js"]