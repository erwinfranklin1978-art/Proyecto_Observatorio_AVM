# Observatorio Inmobiliario Inteligente + AVM
## Visión y Blueprint del Proyecto

Autor: Erwin Franklin Ramírez  
Perfil: Avaluador RAA – Analista de Datos – Desarrollador de Software  
Año: 2026  

---

# 1. Información General del Proyecto

## Nombre del Proyecto
Observatorio Inmobiliario Inteligente + AVM (Automated Valuation Model)

## Tipo de Proyecto
Sistema de análisis de mercado inmobiliario basado en ciencia de datos, geoinformación y modelos de machine learning para estimación automática del valor comercial de inmuebles.

## Estado del Proyecto
Fase inicial de desarrollo (MVP).

---

# 2. Problema que Resuelve

El mercado inmobiliario presenta varios problemas estructurales que dificultan el análisis técnico y la valoración objetiva de los inmuebles.

## Falta de información estructurada

La información del mercado inmobiliario se encuentra dispersa en múltiples portales y fuentes:

- portales inmobiliarios
- inmobiliarias locales
- anuncios informales
- informes de avalúo
- datos catastrales

Esto genera:

- baja trazabilidad
- poca transparencia
- dificultad para realizar análisis comparativos.

---

## Procesos manuales en avalúos

Los estudios de mercado para avalúos implican:

- búsqueda manual de comparables
- revisión de múltiples portales
- consolidación manual de datos
- análisis subjetivo del mercado

Este proceso genera una gran cantidad de **trabajo repetitivo (grunt work)** que podría ser automatizado mediante herramientas de ciencia de datos.

---

## Falta de herramientas analíticas

En muchos mercados locales no existen:

- observatorios inmobiliarios abiertos
- bases de datos históricas del mercado
- herramientas analíticas geoespaciales
- modelos de estimación automática de valor

Esto limita la toma de decisiones para:

- avaluadores
- inversionistas
- inmobiliarias
- entidades financieras

---

# 3. Objetivo del Proyecto

## Objetivo General

Desarrollar un **Observatorio Inmobiliario Inteligente** que permita recolectar, procesar, analizar y visualizar datos del mercado inmobiliario y construir un **Modelo Automatizado de Avalúos (AVM)** basado en datos reales de mercado.

---

## Objetivos Específicos

1. Automatizar la captura de ofertas inmobiliarias desde portales web.
2. Construir una base de datos histórica del mercado inmobiliario.
3. Visualizar el mercado mediante mapas interactivos.
4. Analizar patrones y tendencias del mercado inmobiliario.
5. Entrenar modelos de machine learning para estimación de valor.
6. Generar reportes automáticos de valor comercial.
7. Monetizar el sistema mediante suscripciones y reportes especializados.

---

# 4. Alcance del MVP

El sistema en su versión inicial se enfocará en:

## Tipo de inmuebles

- vivienda urbana
- apartamentos
- casas urbanas

## Ubicación geográfica

- Cali
- Palmira

## Tipo de análisis

- análisis de oferta inmobiliaria
- análisis de precio por metro cuadrado
- detección automática de comparables
- estimación automática de valor (AVM)

---

# 5. Arquitectura General del Sistema

El sistema se compone de seis módulos principales.
uentes de datos
↓
Web Scraping / Ingesta
↓
Procesamiento ETL
↓
Base de Datos Geoespacial
↓
Modelos de Machine Learning
↓
API
↓
Frontend / Observatorio

---

# 6. Fuentes de Datos

El observatorio integrará múltiples fuentes de información.

## Portales inmobiliarios

Ejemplos:

- FincaRaiz
- MetroCuadrado
- Properati
- OLX

Estos portales contienen información sobre:

- precios de oferta
- características del inmueble
- ubicación aproximada
- fotografías y descripciones.

---

## Datos abiertos

Se utilizarán también datasets geográficos como:

- barrios
- comunas
- cartografía urbana
- límites administrativos
- equipamientos urbanos

---

## Informes de avalúo

El sistema también podrá utilizar:

PDF de informes de avalúos existentes.

Estos documentos contienen información valiosa como:

- ubicación del inmueble
- áreas
- características constructivas
- comparables utilizados
- valor final del avalúo

Estos datos pueden alimentar datasets de entrenamiento para modelos AVM.

---

# 7. Arquitectura de Datos

El sistema utilizará una arquitectura de datos basada en tres niveles.
RAW DATA
Datos capturados sin procesar

↓

CLEAN DATA
Datos normalizados y depurados

↓

CURATED DATA
Datos listos para análisis y modelos

---

## Tabla principal: ofertas_inmobiliarias

Campos principales:

- id
- fuente
- fecha_captura
- precio
- area_construida
- area_terreno
- precio_m2
- tipo_inmueble
- habitaciones
- banos
- garajes
- estrato
- direccion
- barrio
- comuna
- latitud
- longitud
- descripcion
- url

---

## Tabla: historico_precios

Permite analizar cambios de precio en el tiempo.

---

## Tabla: comparables

Contiene comparables curados utilizados en avalúos.

---

## Tabla: dataset_avm

Dataset utilizado para entrenamiento de modelos.

---

# 8. Arquitectura de Machine Learning

El AVM se basa en modelos de aprendizaje supervisado.

## Variables predictoras

Ejemplos:

- área construida
- área del terreno
- ubicación geográfica
- barrio
- estrato
- habitaciones
- baños
- garajes
- antigüedad
- estado de conservación
- piso
- ascensor
- cercanía a equipamientos urbanos

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

# 9. Arquitectura API

El sistema expondrá una API REST que permitirá consultar datos del observatorio.

Ejemplo de endpoints:
/ofertas
/ofertas/{id}
/comparables
/zonas
/avaluar
/indicadores

---

# 10. Frontend del Observatorio

El frontend permitirá visualizar el mercado inmobiliario mediante herramientas interactivas.

## Funcionalidades

- mapa interactivo de ofertas
- filtros por zona
- análisis de precios
- visualización de comparables
- consulta de valor estimado

---

## Herramienta de avalúo

El usuario podrá ingresar variables como:

- área
- habitaciones
- baños
- garaje
- barrio

Y el sistema estimará el valor comercial del inmueble.

---

# 11. Monetización del Sistema

El sistema podrá monetizar mediante diferentes mecanismos.

## Suscripción

Acceso al observatorio inmobiliario.

---

## Reportes

Venta de reportes especializados:

- reportes de mercado
- análisis por zona
- comparables inmobiliarios
- estimaciones AVM

---

## API

Acceso a la API para:

- inmobiliarias
- constructoras
- bancos
- inversionistas

---

# 12. Roadmap del Proyecto

## Fase 1
Arquitectura del sistema y captura inicial de datos.

## Fase 2
Construcción de base de datos y análisis exploratorio (EDA).

## Fase 3
Desarrollo del Observatorio Inmobiliario (MVP).

## Fase 4
Entrenamiento del modelo AVM versión 1.

## Fase 5
Desarrollo de API y modelo de monetización.

---

# 13. Estructura del Repositorio
01_documentacion
02_data
03_notebooks
04_scraping
05_api
06_frontend
07_modelos

Esta estructura separa claramente:

- documentación
- datos
- análisis
- scraping
- backend
- frontend
- modelos de machine learning

---

# 14. Visión a Largo Plazo

El proyecto puede evolucionar hacia una plataforma PropTech que integre:

- analítica inmobiliaria
- valoración automática
- inteligencia geoespacial
- análisis de inversión inmobiliaria

Esta plataforma podría convertirse en una herramienta clave para la toma de decisiones en el mercado inmobiliario.