# 🚀 Automatización de Infraestructura con n8n, Ansible y GitHub Actions

Este proyecto permite automatizar la creación y configuración de máquinas virtuales a partir de los requisitos proporcionados por un cliente, utilizando un flujo DevOps completo basado en Infrastructure as Code y CI/CD.

El objetivo es que el cliente únicamente indique qué quiere instalar y dónde, y el sistema se encargue automáticamente del resto.

---

## Arquitectura General

Flujo del sistema:

Cliente → Formulario Web → n8n → Repositorio GitHub → GitHub Actions → Ansible → Máquina Virtual

## Requisitos Previos

Antes de ejecutar el workflow es necesario:

- Una máquina virtual Linux accesible por SSH
- Conocer:
  - Usuario SSH
  - Contraseña SSH
- Un repositorio de GitHub con Actions habilitado

---

## Configuración de Secretos en GitHub

Por seguridad, las credenciales no se incluyen en el código.  
Es obligatorio configurar los siguientes **GitHub Secrets**:

| Nombre del secreto | Descripción |
|--------------------|------------|
| `ANSIBLE_SSH_PASS` | Contraseña SSH del usuario remoto |
