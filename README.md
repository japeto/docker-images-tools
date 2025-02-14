# Docker Environments

This repository provides two Docker environments, one with basic development tools and another with support for parallel computing using MPI and OpenMP.

## 🛠️ Available Images
1. **GCC Development Tools (`so-tools`)**
   - Based on `gcc:4.9`
   - Includes `vim` and `nano` for editing code inside the container.
   - [docker pull japeto/so-tools](https://hub.docker.com/r/japeto/so-tools)

2. **GCC with MPI & OpenMP (`parallel-tools`)**
   - Supports **MPI (Message Passing Interface)** with OpenMPI.
   - OpenMP support included via GCC.
   - [docker pull japeto/parallel-tools](https://hub.docker.com/r/japeto/parallel-tools)

## 🚀 How to Build and Run

### **1️⃣ GCC Tools Image**
```sh
docker build --platform linux/arm64 -t japeto/so-tools ./so-tools
docker run -it --rm japeto/so-tools
```

### **2️⃣  GCC with MPI & OpenMP Image**
```sh
docker build --platform linux/arm64 -t japeto/parallel-tools ./parallel-tools
docker run -it --rm japeto/parallel-tools
```