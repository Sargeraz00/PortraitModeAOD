# StandBy Mode for Android

![Status](https://img.shields.io/badge/Status-Development-orange)
![Platform](https://img.shields.io/badge/Platform-Android-green)
![Device](https://img.shields.io/badge/Optimized-Samsung%20S24%20Ultra-blue)

Una aplicación diseñada para replicar la experiencia "StandBy" de iOS en dispositivos Android, con optimizaciones específicas para el Samsung Galaxy S24 Ultra y otros dispositivos con pantallas AMOLED.

## 🚀 Visión del Proyecto

La aplicación activa automáticamente una interfaz informativa y estética cuando se cumplen tres condiciones clave:
1. **Carga Inalámbrica activa:** Detecta cargadores Qi o MagSafe.
2. **Orientación Horizontal:** El dispositivo está colocado de lado (Landscape).
3. **Pantalla de Bajo Consumo:** Una interfaz optimizada estilo Always On Display (AOD).

## ✨ Características Principales

- **Detección Inteligente:** Activación automática mediante sensores sin intervención del usuario.
- **Interfaz AOD Extendida:** Relojes digitales y analógicos de gran formato.
- **Widgets Modulares:** Visualización de calendario, clima, notificaciones y controles de música.
- **Optimización Anti-Burn-in:** Implementación de "pixel shifting" y fondos negros puros (AMOLED).
- **Personalización:** Ajustes de color, estilo y selección de datos a mostrar.

## 🏗️ Arquitectura y Estructura

El proyecto sigue los principios de **Clean Architecture** y **MVVM (Model-View-ViewModel)** para garantizar un código mantenible, escalable y testeable.

### Estructura de Carpetas

```text
App
├── Core         # Utilidades compartidas y extensiones base
├── Di           # Configuración de Inyección de Dependencias (Hilt)
├── Utils        # Funciones de utilidad general
├── Network      # Clientes API y configuración de red
└── Features     # Módulos basados en funcionalidades
    ├── Standby  # Módulo principal de la vista StandBy
    │   ├── Domain # Casos de uso y modelos de negocio
    │   ├── Data   # Repositorios y fuentes de datos
    │   └── Presentation # UI (Jetpack Compose) y ViewModels
    └── Settings # Gestión de preferencias del usuario
        ├── Domain
        ├── Data
        └── Presentation
```

## 🛠️ Tecnologías

- **Kotlin:** Lenguaje principal.
- **Jetpack Compose:** Para una UI moderna y reactiva.
- **Hilt:** Inyección de dependencias.
- **DataStore:** Persistencia de preferencias.
- **Lifecycle Service:** Para la gestión eficiente de sensores en segundo plano.

## 📅 Hoja de Ruta (Roadmap)

- [x] **Fase 1:** Infraestructura y Definición de Guías.
- [ ] **Fase 2:** Implementación de Sensores y Detección (Carga/Orientación).
- [ ] **Fase 3:** Desarrollo de UI Base y Display Manager.
- [ ] **Fase 4:** Integración de Widgets y Personalización.
- [ ] **Fase 5:** Optimización Energética y Pulido Final.

## 📱 Requisitos

- Android 10 (API 29) o superior.
- Pantalla AMOLED (Recomendado para eficiencia energética).
- Sensor de Gravedad/Acelerómetro.

---
Desarrollado con ❤️ para la comunidad de Android.
