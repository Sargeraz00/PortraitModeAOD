# StandBy Mode for Android

[Español](#español) | [English](#english)

---

<a name="español"></a>
# 🇪🇸 StandBy Mode for Android (Español)

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

## 🌿 Estrategia de Ramas (Branching Strategy)

Para mantener un flujo de desarrollo organizado, seguimos la siguiente política de branching:

- **`master`**: Rama principal que contiene el código en producción.
- **`develop`**: Rama de integración. Aquí se consolidan todas las funcionalidades terminadas antes de pasar a producción.
- **`feature/`**: Ramas para nuevas funcionalidades. Se integran a `develop` únicamente mediante **Pull Request (PR)**.
- **`task/`**: Ramas de tareas específicas y granulares. Se integran a su respectiva `feature/` mediante **merge directo**.
- **`hotfix/`**: Ramas para correcciones críticas en producción. Se integran directamente a `master` mediante **PR aprobado por el administrador** y posteriormente se sincronizan con `develop`.

### Convención de Nombres (Nomenclatura)
Se debe utilizar **camelCase** para los nombres descriptivos:
- **Features:** `feature/feature-nombreDeLaFeature`
- **Tasks:** `task/task-nombreDeLaTarea`
- **Hotfixes:** `hotfix/hotfix-descripcionDelError`

### Flujo de Integración
1. `task/*` ➡️ `feature/*` (Merge directo)
2. `feature/*` ➡️ `develop` (Vía Pull Request)
3. `hotfix/*` ➡️ `master` (Vía Pull Request - Solo Admin)
4. `develop` ➡️ `master` (Vía Pull Request - Solo Admin)

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

<a name="english"></a>
# 🇺🇸 StandBy Mode for Android (English)

![Status](https://img.shields.io/badge/Status-Development-orange)
![Platform](https://img.shields.io/badge/Platform-Android-green)
![Device](https://img.shields.io/badge/Optimized-Samsung%20S24%20Ultra-blue)

An application designed to replicate the iOS "StandBy" experience on Android devices, with specific optimizations for the Samsung Galaxy S24 Ultra and other AMOLED display devices.

## 🚀 Project Vision

The app automatically triggers an aesthetic and informative interface when three key conditions are met:
1. **Active Wireless Charging:** Detects Qi or MagSafe chargers.
2. **Horizontal Orientation:** The device is placed on its side (Landscape).
3. **Low Power Display:** An optimized Always On Display (AOD) style interface.

## ✨ Key Features

- **Smart Detection:** Automatic activation via sensors without user intervention.
- **Extended AOD Interface:** Large format digital and analog clocks.
- **Modular Widgets:** View calendar, weather, notifications, and music controls.
- **Anti-Burn-in Optimization:** Implementation of "pixel shifting" and pure black backgrounds (AMOLED).
- **Customization:** Color, style settings, and data selection to display.

## 🏗️ Architecture & Structure

The project follows **Clean Architecture** and **MVVM (Model-View-ViewModel)** principles to ensure maintainable, scalable, and testable code.

### Folder Structure

```text
App
├── Core         # Shared utilities and base extensions
├── Di           # Dependency Injection configuration (Hilt)
├── Utils        # General utility functions
├── Network      # API clients and network configuration
└── Features     # Feature-based modules
    ├── Standby  # Main StandBy view module
    │   ├── Domain # Use cases and business models
    │   ├── Data   # Repositories and data sources
    │   └── Presentation # UI (Jetpack Compose) and ViewModels
    └── Settings # User preferences management
        ├── Domain
        ├── Data
        └── Presentation
```

## 🛠️ Technologies

- **Kotlin:** Main language.
- **Jetpack Compose:** For a modern and reactive UI.
- **Hilt:** Dependency Injection.
- **DataStore:** Preference persistence.
- **Lifecycle Service:** For efficient background sensor management.

## 🌿 Branching Strategy

To maintain an organized development flow, we follow this branching policy:

- **`master`**: Main branch containing production code.
- **`develop`**: Integration branch. All finished features are consolidated here before moving to production.
- **`feature/`**: Branches for new features. They integrate into `develop` solely via **Pull Request (PR)**.
- **`task/`**: Specific and granular task branches. They integrate into their respective `feature/` via **direct merge**.
- **`hotfix/`**: Branches for critical production fixes. They integrate directly into `master` via **Admin-approved PR** and are later synchronized with `develop`.

### Naming Convention
**camelCase** must be used for descriptive names:
- **Features:** `feature/feature-featureName`
- **Tasks:** `task/task-taskName`
- **Hotfixes:** `hotfix/hotfix-errorDescription`

### Integration Flow
1. `task/*` ➡️ `feature/*` (Direct Merge)
2. `feature/*` ➡️ `develop` (Via Pull Request)
3. `hotfix/*` ➡️ `master` (Via Pull Request - Admin Only)
4. `develop` ➡️ `master` (Via Pull Request - Admin Only)

## 📅 Roadmap

- [x] **Phase 1:** Infrastructure and Guidelines Definition.
- [ ] **Phase 2:** Sensor Implementation and Detection (Charging/Orientation).
- [ ] **Phase 3:** Base UI and Display Manager Development.
- [ ] **Phase 4:** Widget Integration and Customization.
- [ ] **Phase 5:** Energy Optimization and Final Polish.

## 📱 Requirements

- Android 10 (API 29) or higher.
- AMOLED Display (Recommended for energy efficiency).
- Gravity Sensor/Accelerometer.

---
Developed with ❤️ for the Android community.
