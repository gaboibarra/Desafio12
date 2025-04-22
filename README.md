# 📦 Helm Chart – `educacionit-app` + MongoDB

Este proyecto desarrolla un Helm Chart personalizado para desplegar la aplicación `educacionit-app` junto a una base de datos MongoDB, cumpliendo con los requisitos del Desafío 12 del DevOps Bootcamp.

---

## 🎯 Objetivo

✅ Eliminar la duplicación de manifiestos YAML  
✅ Utilizar Helm para generar templates reutilizables  
✅ Gestionar correctamente los deployments de la app y MongoDB  
✅ Documentar el proceso completo y evidenciar despliegue exitoso  

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
