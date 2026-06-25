# Sistema Automatizado de Registro Vehicular (BUAP)

Aplicación móvil nativa en Android (Java) para el control de acceso vehicular en la BUAP mediante escaneo automático de placas con Reconocimiento Óptico de Caracteres (OCR). Desarrollada como un Producto Mínimo Viable (MVP) con arquitectura de almacenamiento 100% local.

---

## Estructura de Directorios y Módulos

La arquitectura del proyecto divide la aplicación en cuatro módulos principales para facilitar el desarrollo en paralelo y asegurar la separación de responsabilidades:

```text
RegistroVehicularBUAP/
│
├── app/src/main/java/com/buap/registrovehicular/
│   │
│   ├── ui/                     #  Módulo de Interfaz y Navegación
│   │   ├── MainActivity.java   # Pantalla principal (Inicio de sesión)
│   │   ├── ScannerActivity.java# Pantalla de la cámara y estado de validación (Verde/Rojo)
│   │   └── HistoryActivity.java# Pantalla para visualizar la tabla de registros del día
│   │
│   ├── ocr/                    #  Módulo de Visión por Computadora
│   │   └── TextAnalyzer.java   # Captura el frame de la cámara, usa ML Kit y extrae el texto
│   │
│   ├── data/                   #  Módulo de Base de Datos Local
│   │   ├── localdb/            # Configuración e inicialización de la base de datos Realm
│   │   └── model/              # Modelos Orientados a Objetos (Ej. AccesoLog, Vehiculo, Usuario)
│   │
│   └── app/src/main/res/           # Recursos Visuales
│   ├── layout/                 # Diseños XML de las interfaces
│   ├── drawable/               # Íconos, botones y recursos gráficos
│   └── values/                 # Paleta de colores institucionales y textos
