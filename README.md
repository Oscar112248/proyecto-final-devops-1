# 🚀 Proyecto Final DevOps

[![Docker Image](https://img.shields.io/badge/Docker-Image-blue?style=for-the-badge&logo=docker)](https://hub.docker.com/r/tu-usuario/devops-final-project)
[![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-Automated-2088FF?style=for-the-badge&logo=github-actions)](https://github.com/tu-usuario/tu-repo/actions)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.115.0-009688?style=for-the-badge&logo=fastapi)](https://fastapi.tiangolo.com/)
[![Python](https://img.shields.io/badge/Python-3.12-3776AB?style=for-the-badge&logo=python)](https://www.python.org/)

---

## 📃Resumen Ejecutivo

| Elemento | Descripción |
| --- | --- |
| Proyecto | Aplicacion web desarrollada con FastAPI para el Trabajo Final DevOps |
| Objetivo | Despliegue mediante GitHub Actions |
| Enfoque técnico | Desarrollo por ramas con Gitflow, publica la imagen en Docker Hub mediante GitHub Actions |
| Versión entregable | `v1.0.0` |
| Autores | Oscar Maldonado, Daniel Alquinga |

---

## ✳️ Descripción del Proyecto

Aplicacion web desarrollada con FastAPI para el Trabajo Final DevOps. El proyecto construye una imagen Docker, publica la imagen en Docker Hub mediante GitHub Actions y expone una pagina de verificacion con informacion del grupo y del contenedor.

---

## 📚Funcionalidades

- ✅ **Contenerización** con Docker
- ✅ **Integración Continua** con GitHub Actions
- ✅ **Publicación automatizada** en Docker Hub
- ✅ **Infraestructura como Código** (Dockerfile)
- ✅ **Health Checks** para monitoreo
- ✅ **Variables de entorno** para configuración
---

## 🏛️ Componentes del Sistema

| Componente | Tecnología | Función |
|------------|------------|---------|
| **Código Fuente** | Python + FastAPI | Lógica de la aplicación web |
| **Control de Versiones** | GitHub | Almacenamiento y versionado del código |
| **CI/CD Pipeline** | GitHub Actions | Automatización de build y deploy |
| **Contenerización** | Docker | Empaquetado y portabilidad |
| **Registro de Imágenes** | Docker Hub | Almacenamiento y distribución de imágenes |
| **Health Check** | FastAPI + Docker | Monitoreo de estado del contenedor |
---

## 📊 Diagrama de Arquitectura
```mermaid
graph LR
    A[Código Fuente] --> B[GitHub]
    B --> C[GitHub Actions]
    C --> D[Build Docker Image]
    D --> E[Push a Docker Hub]
    E --> F[Pull y Ejecución]
    
    style A fill:#f9f,stroke:#333,stroke-width:2px
    style B fill:#f9f,stroke:#333,stroke-width:2px
    style C fill:#bbf,stroke:#333,stroke-width:2px
    style D fill:#bfb,stroke:#333,stroke-width:2px
    style E fill:#fbb,stroke:#333,stroke-width:2px
    style F fill:#bfb,stroke:#333,stroke-width:2px
```
---

## 📋 Flujo del Pipeline
```mermaid
sequenceDiagram
    participant D as Desarrollador
    participant G as GitHub
    participant A as GitHub Actions
    participant H as Docker Hub
    
    D->>G: Push a main / Tag v1
    G->>A: Trigger workflow
    A->>A: 1. Checkout repository
    A->>A: 2. Setup Docker Buildx
    A->>H: 3. Login (secrets)
    A->>A: 4. Build image
    A->>H: 5. Push image
    H-->>A: ✅ Confirmación
    A-->>G: ✅ Pipeline exitoso
```
---
## 📂 Estructura Del Proyecto

```text
proyecto-final-devops
|-- app
|   |-- main.py
|   `-- templates
|       `-- index.html
|-- .github
|   `-- workflows
|       `-- dockerhub.yml
|-- .dockerignore
|-- .gitignore
|-- Dockerfile
|-- INFORME.md
|-- README.md
|-- VERSION
`-- requirements.txt
```

---

## 💾 Instalación

[![Informe Instalación](https://img.shields.io/badge/INSTALACIÓN-verde?style=for-the-badge)](./INFORME.md)

## 👬Autores

| Integrante | Rol | Url Git |
| --- | --- | --- |
| Oscar Maldonado | Desarrollo, documentación y control de versiones | https://github.com/Oscar112248/proyecto-final-devops/tree/main |
| Daniel Alquinga | Validación funcional, revisión y evidencias | https://github.com/superdavi/proyecto-final-devops/tree/main |
