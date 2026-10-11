# CST8915 Lab 4 – Algonquin Pet Store Part 3

**Student Name**: Abdullahi Omer
**Student ID**: 09043215
**Course**: CST8915 Full-stack Cloud-native Development
**Semester**: Fall 2026

---

## Demo Video

🎥 [Watch Demo Video](https://youtu.be/zorqu8Voq_g)

---

## Reflection Questions

### 1. What are the main differences between a Docker image and a Docker container?

A Docker image is a template that contains the application code, dependencies, and configurations needed to run an application. A container is a running instance of that image. Images are read-only, while containers can make changes through their own writable layer. Multiple containers can also be created from the same image.

### 2. Explain how Docker's layered architecture improves efficiency.

Docker builds images in layers, allowing it to reuse layers that have not changed instead of rebuilding everything. For example, when I modified the Flask application, Docker could reuse the previously built dependency layers. This saves time during builds and reduces storage usage since images can share layers.

### 3. Why does each container get its own writable layer?

Each container gets its own writable layer so it can store changes without affecting other containers using the same image. In the lab, I created three containers from one image and added a different text file to each. The files remained separate, showing how containers can run independently while sharing the same image.

### 4. What are the benefits of using Docker Compose over running containers individually?

Docker Compose makes it easier to manage multiple containers using a single YAML file. Instead of running separate commands for each container, I can define their ports, images, and configurations in one place. I can also start or stop all the containers with one command, which makes managing applications with multiple services easier.
