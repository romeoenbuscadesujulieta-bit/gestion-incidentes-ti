# Gestión de Incidentes TI - Etapa 3

Repositorio oficial del proyecto integrador.

## Diagrama Funcional del Sistema
```mermaid
graph TD
    A[1. Usuario ingresa datos del incidente] --> B[2. Validación de datos en la App]
    B --> C{¿Hay conexión a Internet?}
    C -- Sí --> D[(Cloud Firestore - Firebase)]
    C -- No --> E[(Base de Datos Local - SQLite)]
    D --> F[3. Actualización de pantalla en tiempo real]
    E --> F
