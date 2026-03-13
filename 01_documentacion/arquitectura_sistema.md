# Arquitectura del Sistema
## Observatorio Inmobiliario Inteligente + AVM

Autor: Erwin Franklin Ramírez  
Proyecto: Observatorio Inmobiliario + Modelo Automatizado de Avalúos  
Año: 2026

---

# 1. Introducción

Este documento describe la arquitectura tecnológica del sistema **Observatorio Inmobiliario Inteligente + AVM**, una plataforma diseñada para recopilar, analizar y visualizar datos del mercado inmobiliario y estimar el valor comercial de inmuebles mediante modelos de Machine Learning.

La arquitectura está orientada a:

- análisis de datos
- procesamiento geoespacial
- modelos de inteligencia artificial
- visualización interactiva
- generación automática de reportes

---

# 2. Arquitectura General del Sistema

El sistema sigue una arquitectura modular basada en capas.

Fuentes de Datos
↓
Ingesta de Datos (Scraping / APIs)
↓
Procesamiento ETL
↓
Base de Datos Geoespacial
↓
Motor Analítico y Machine Learning
↓
API Backend
↓
Frontend / Observatorio


---

# 3. Componentes del Sistema

El sistema está compuesto por los siguientes módulos principales.

## 3.1 Módulo de Ingesta de Datos

Responsable de capturar información del mercado inmobiliario desde diferentes fuentes.

### Fuentes

- portales inmobiliarios
- datos abiertos
- informes de avalúo
- registros manuales

### Tecnologías

- Python
- Requests
- BeautifulSoup
- Selenium (si es necesario)

---

## 3.2 Módulo ETL (Extract, Transform, Load)

Este módulo procesa y limpia los datos capturados.

### Funciones principales

- limpieza de datos
- normalización de variables
- eliminación de duplicados
- cálculo de precio por metro cuadrado
- validación de datos

### Tecnologías

- Python
- Pandas
- GeoPandas

---

## 3.3 Base de Datos Geoespacial

El sistema utilizará una base de datos relacional con soporte geográfico.

### Tecnología

PostgreSQL + PostGIS

### Ventajas

- manejo de coordenadas geográficas
- consultas espaciales
- integración con herramientas GIS

---

## 3.4 Motor de Machine Learning

Este módulo implementa los modelos AVM.

### Funciones

- entrenamiento de modelos
- validación
- predicción de valores
- monitoreo de desempeño

### Tecnologías

- Python
- Scikit-learn
- XGBoost
- LightGBM

---

## 3.5 API Backend

La API permite que el frontend y otros sistemas consulten el observatorio.

### Tecnología

FastAPI

### Endpoints principales
/ofertas
/comparables
/zonas
/avaluar
/indicadores


---

## 3.6 Frontend del Observatorio

Interfaz web para visualizar el mercado inmobiliario.

### Funcionalidades

- mapa interactivo
- filtros de búsqueda
- dashboard analítico
- consulta de valor estimado

### Tecnologías

- React
- Leaflet
- Mapbox

---

# 4. Arquitectura de Datos

El sistema utilizará un modelo de arquitectura de datos en tres niveles.

RAW DATA
Datos capturados sin procesar

↓

CLEAN DATA
Datos normalizados

↓

CURATED DATA
Datos preparados para análisis y modelos


---

# 5. Pipeline de Datos

El pipeline de datos sigue el siguiente flujo.

Scraping
↓
Limpieza de datos
↓
Normalización
↓
Geocodificación
↓
Almacenamiento
↓
Análisis
↓
Entrenamiento de modelos


---

# 6. Arquitectura del AVM

El modelo AVM utilizará aprendizaje supervisado.

## Variables del modelo

- área construida
- área del terreno
- ubicación
- estrato
- habitaciones
- baños
- garajes
- antigüedad
- estado del inmueble

---

## Modelos candidatos

- Linear Regression
- Random Forest
- Gradient Boosting
- XGBoost
- LightGBM

---

## Métricas de evaluación

- MAE
- RMSE
- MAPE
- R2

---

# 7. Arquitectura de Seguridad

El sistema implementará medidas básicas de seguridad.

### Autenticación

- login de usuario
- control de roles

### Protección de datos

- cifrado de contraseñas
- acceso restringido a la base de datos

---

# 8. Infraestructura Tecnológica

El sistema podrá desplegarse en infraestructura cloud.

### Opciones

- AWS
- Google Cloud
- Render
- Railway

---

# 9. Estructura del Repositorio

El proyecto utiliza la siguiente estructura.
01_documentacion
02_data
03_notebooks
04_scraping
05_api
06_frontend
07_modelos


---

# 10. Escalabilidad del Sistema

El sistema está diseñado para permitir:

- incorporación de nuevas ciudades
- integración de nuevas fuentes de datos
- mejoras en los modelos ML
- ampliación del observatorio

---

# 11. Evolución Tecnológica

En fases futuras el sistema podrá incluir:

- análisis predictivo de precios
- detección de oportunidades de inversión
- integración con datos catastrales
- integración con sistemas financieros