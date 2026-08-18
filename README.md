# Tônus - Fitness & Gym Tracker

Tônus es una aplicación móvil para Android desarrollada en Java, orientada al seguimiento detallado de entrenamientos, gestión de rutinas, control de métricas corporales y análisis de progreso mediante inteligencia artificial.

---

## Tabla de Contenidos
- [Características Principales](#características-principales)
- [Historias de Usuario](#historias-de-usuario)
- [Tecnologías Utilizadas](#tecnologías-utilizadas)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Instalación y Configuración](#instalación-y-configuración)
- [Licencia](#licencia)

---

## Características Principales

### Autenticación y Gestión de Usuario
- Registro con correo electrónico, nombre de usuario y contraseña.
- Envío de correo de verificación para confirmación de cuenta.
- Mantener la sesión activa inmediatamente después del registro.

### Biblioteca de Ejercicios
- Organización por grupo muscular (Pecho, Espalda, Piernas, Core), subtipo (Cuádriceps, Dorsal, Femoral, Pecho Superior) y tipo de ejercicio (Máquina, Pesas libres).
- Imágenes ilustrativas, descripción y guía paso a paso para la correcta ejecución.
- Solicitud de incorporación de nuevos ejercicios en caso de no encontrarlos.

### Creación y Gestión de Rutinas
- Diseñador de rutinas personalizadas seleccionando ejercicios del banco general.
- Asignación de nombres personalizados y guardado en biblioteca propia.
- Catálogo de rutinas pre-armadas organizadas por nivel u objetivo con opción de clonación directa a la biblioteca personal.

### Seguimiento de Entrenamiento y Descansos
- Definición de parámetros por serie: repeticiones, tipo de serie (Normal, Superserie, Dropset) y registro de horas/duración.
- Selector dinámico de unidades de peso entre kilogramos (kg) y libras (lbs).
- Edición y actualización libre de parámetros en cualquier momento.
- Marcas de verificación (check) para dar por completada cada serie.
- Temporizador interactivo de descanso al marcar una serie, con botón para añadir +5 segundos y notificaciones internas al finalizar la cuenta regresiva.

### Métricas Corporales y Calculadora IMC
- Registro histórico de medidas corporales, peso y altura ordenados por fecha.
- Recordatorios semanales para la toma de medidas.
- Calculadora automática del Índice de Masa Corporal (IMC) basada en peso, altura y nivel de actividad guardados, indicando la condición física actual del usuario.

### Análisis e Integración con Inteligencia Artificial
- Visualización de volumen de entrenamiento semanal en gráficos organizados por grupo muscular.
- Integración con API de Inteligencia Artificial para ofrecer recomendaciones personalizadas sobre la rutina.
- Evaluación de imágenes corporales mediante IA para ofrecer consejos de mejora y ajustar el esquema de entrenamiento (split) actual.

### Interfaz y Configuración
- Soporte multilingüe (traducción de la interfaz y nombres de ejercicios a diferentes idiomas).
- Selección de modo de interfaz: Tema Claro y Tema Oscuro.
- Diseño accesible, directo e intuitivo para el usuario.

---

## Historias de Usuario

| ID | Título | Descripción / Criterios de Aceptación | Prioridad | Estimación |
|:---|:---|:---|:---:|:---:|
| US-01 | Register y Login | Formulario con correo, usuario y contraseña. Envío de correo de verificación y sesión iniciada tras registro. | HIGH | 14 horas |
| US-02 | Biblioteca de Ejercicios | Consulta de ejercicios agrupados por músculo, subtipo y equipo, con imagen, instrucciones y solicitud de nuevos ítems. | HIGH | 12 horas |
| US-03 | Crear Rutinas Personalizadas | Banco categorizado para seleccionar múltiples ejercicios, asignar nombre y guardar en la biblioteca propia. | HIGH | 20 horas |
| US-04 | Detalles del Entrenamiento | Entrada de reps, tipo de serie (normal, superserie, dropset), duración, selector kg/lbs y check de serie completada. | MEDIUM | 12 horas |
| US-05 | Manejo de Descansos | Configuración del tiempo de descanso, inicio de temporizador tras check, sumador +5s y notificación interna al terminar. | MEDIUM | 13 horas |
| US-06 | Registro en Grafos | Resumen semanal gráfico de series por grupo muscular y recomendaciones automáticas de entrenamiento mediante IA. | MEDIUM | 12 horas |
| US-07 | Guardar Métricas | Registro por fecha de altura, peso y medidas corporales para comparación de progreso, con recordatorio semanal. | LOW | 8 horas |
| US-08 | Calculador de IMC | Módulo de cálculo automático de IMC usando peso, altura e índice de actividad almacenados, con diagnóstico de condición. | LOW | 6 horas |
| US-09 | Recibir Imagen de IA | Subida de fotografía del usuario para análisis con IA, cruzando datos con la rutina activa para brindar consejos de mejora. | LOW | 20 horas |
| US-10 | Rutinas Pre-establecidas | Catálogo de rutinas prediseñadas con vista previa detallada y función para clonarlas a la colección personal. | LOW | 10 horas |
| US-11 | Traducción del Programa | Soporte multilingüe para textos de la aplicación y nombres/descripciones de ejercicios. | MEDIUM | N/A |
| US-12 | Modo Interfaz | Conmutación entre paleta de colores clara y oscura en la interfaz. | LOW | N/A |

---

## Tecnologías Utilizadas

- **Lenguaje de Programación:** Java
- **Plataforma:** Android SDK
- **Sistema de Construcción:** Gradle KTS (`build.gradle.kts`)
- **Arquitectura:** Android Architecture Components (MVVM)
- **Integración de IA:** API REST de Visión por Computadora y Procesamiento de Lenguaje
- **Notificaciones:** Sistema de notificaciones locales de Android

---

## Estructura del Proyecto

```text
Tônus/
├── .gradle/               # Archivos de caché del motor Gradle
├── .idea/                 # Configuración del entorno de desarrollo Android Studio
├── app/                   # Módulo principal con el código fuente Java y recursos
│   ├── src/               # Código Java, layouts XML y recursos visuales
│   └── build.gradle.kts   # Dependencias y configuración del módulo app
├── build/                 # Archivos compilados generados
├── gradle/                # Configuración del wrapper de Gradle
├── .gitignore             # Exclusión de archivos en control de versiones Git
├── build.gradle.kts       # Configuración global del proyecto Gradle
├── gradle.properties      # Propiedades del entorno Gradle
├── gradlew                # Script ejecutable de Gradle para sistemas Unix/Linux/macOS
├── gradlew.bat            # Script ejecutable de Gradle para Windows
├── local.properties       # Rutas del SDK local (excluido de Git)
├── README.md              # Documentación del repositorio
└── settings.gradle.kts    # Configuración de inclusión de módulos
