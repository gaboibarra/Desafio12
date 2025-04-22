# 📦 Helm Chart – `educacionit-app` + MongoDB

Este proyecto desarrolla un Helm Chart personalizado para desplegar la aplicación `educacionit-app` junto a una base de datos MongoDB, cumpliendo con los requisitos del Desafío 12 del DevOps Bootcamp.

---

## 🎯 Objetivo

✅ Eliminar la duplicación de manifiestos YAML  
✅ Utilizar Helm para generar templates reutilizables  
✅ Gestionar correctamente los deployments de la app y MongoDB  
✅ Documentar el proceso completo y evidenciar despliegue exitoso  

---

## ⚙️ Instalar Helm - (En este caso via Chocolatey Windows)

![image](https://github.com/user-attachments/assets/46cd76f1-b298-4549-8206-1e84ed29652b)

---

## 🔎 Verificar la instalacion 

![image](https://github.com/user-attachments/assets/8171b206-a5f3-4b89-8914-823ea95a5051)

---

## Crear el Helm Chart

![image](https://github.com/user-attachments/assets/c35d1c55-4056-4c84-93b3-63e6877aeb7b)

---

## 🧱 Estructura del Chart

```bash
educacionit-chart/
├── Chart.yaml
├── values.yaml
└── templates/
    ├── app-deployment.yaml
    ├── app-service.yaml
    ├── mongo-deployment.yaml
    └── mongo-service.yaml
```
## ⚙️ Configuración (`values.yaml`)

![image](https://github.com/user-attachments/assets/07967101-2a36-409e-82bf-97708660236c)

---

## 🧹 Limpieza de archivos por defecto

Al ejecutar helm create educacionit-chart, Helm genera una plantilla completa con varios archivos preconfigurados, como deployment.yaml, service.yaml, ingress.yaml, hpa.yaml, tests/test-connection.yaml, entre otros.
En este desafío el objetivo es construir mis propios archivos personalizados para desplegar una aplicación educacionit-app junto a una base de datos MongoDB, estos archivos por defecto no son necesarios, si los dejo generan errores.
Por este motivo, procedí a eliminarlos para evitar conflictos y mantener el proyecto limpio.

---

## Probar e instalar el Chart

![image](https://github.com/user-attachments/assets/f479dfc3-d2e7-42b3-aac1-ec6df2143e19)

Este error se refiere a que en mi cluster ya hay un educacionit-app desplegado Durante el desarrollo y pruebas de los desafíos anteriores (Desafíos 10 y 11), 
los recursos de Kubernetes como Deployments y Services para la aplicación educacionit-app y la base de datos MongoDB fueron creados manualmente mediante manifiestos YAML aplicados directamente con kubectl.
Para evitar este conflicto, tome la decisión de eliminar todos los recursos creados previamente de forma manual, permitiendo así que Helm pueda desplegar los suyos propios y asumir correctamente la gestión de dichos objetos

---

![image](https://github.com/user-attachments/assets/ab132630-590a-4b53-a4c5-df3c6c99d164)

![image](https://github.com/user-attachments/assets/61d63fdc-564b-424f-8f75-ded6e1eb7bb3)

![image](https://github.com/user-attachments/assets/eeb91be6-be3f-418e-b365-1043ba846c7e)

![image](https://github.com/user-attachments/assets/2ec92494-4a7d-4d7a-bf7d-2fb8ecb0a46e)

---

## 🚀 Instalación del Chart

![image](https://github.com/user-attachments/assets/e5d7f305-0349-4552-bd36-8c06c5e7cd17)

⚠️ Asegurarse de haber eliminado cualquier Deployment, Service o Release previo con el mismo nombre antes de instalar.

---

## 🧪 Verificación del despliegue

![image](https://github.com/user-attachments/assets/3c8fce30-481d-4665-9f70-492d3338d0e7)

Al momento de la captura, los pods aún estaban en proceso de creación (ContainerCreating) debido a la descarga inicial de la imagen desde Docker Hub. Se verificó posteriormente que el estado cambia a Running tras completar el image pull.

---

🧑‍💻 Autor
Gabriel Ibarra – Desafío 12
DevOps Bootcamp – 2024
