# Práctica 4 — Tecnologías de Internet

## Escalado Horizontal, CI/CD con GitHub Actions y GitOps con Flux

---

## Descripción

Esta práctica aborda tres aspectos clave de la operación de aplicaciones en Kubernetes:

1. **Escalado Horizontal (HPA):** configuración del Horizontal Pod Autoscaler para ajustar automáticamente el número de réplicas de la capa frontend en función de la carga de CPU.
2. **CI/CD con GitHub Actions:** automatización de la construcción y publicación de imágenes Docker en GitHub Container Registry (GHCR) ante cambios en el código fuente.
3. **GitOps con Flux:** despliegue continuo basado en GitOps, donde Flux sincroniza el estado del clúster de Kubernetes con el estado definido en este repositorio.

---

## Estructura del repositorio

```
practica4/
├── Plantillas/
│   └── 19-hpa-front.yaml          # Manifiesto HPA para el frontend
├── frontend-files/
│   ├── Dockerfile                  # Dockerfile de la imagen Nginx del frontend
│   └── index.html                  # Página web servida por el frontend
├── flux/
│   └── readme.md
├── k8s/
│   └── readme.md
└── README.md               
```

---

## Requisitos previos

- **Minikube** con Kubernetes ≥ 1.33.0
- **kubectl** configurado contra el clúster
- **Metrics Server** habilitado (`minikube addons enable metrics-server`)
- **Flux CLI** instalado ([instrucciones](https://fluxcd.io/flux/installation/))
- Token de GitHub con permisos `write:packages` y `repo`


## Asignatura

Tecnologías de Internet — Máster Universitario en Ingeniería de Telecomunicación, Universidad de Alcalá
