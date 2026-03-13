# Especificación de Requisitos del Sistema
## Observatorio Inmobiliario Inteligente + AVM

Autor: Erwin Franklin Ramírez  
Proyecto: Observatorio Inmobiliario + Modelo Automatizado de Avalúos (AVM)  
Año: 2026

---

# 1. Introducción

Este documento describe los requisitos funcionales y no funcionales del sistema **Observatorio Inmobiliario Inteligente + AVM**, una plataforma tecnológica diseñada para recopilar, analizar y visualizar información del mercado inmobiliario y estimar valores comerciales de inmuebles mediante modelos de Machine Learning.

El sistema permitirá automatizar parte del proceso de investigación de mercado que tradicionalmente realizan los avaluadores inmobiliarios, proporcionando herramientas de análisis, visualización y estimación automática de valores.

---

# 2. Alcance del Sistema

El sistema permitirá:

- Capturar información de ofertas inmobiliarias desde portales web.
- Construir una base de datos georreferenciada del mercado inmobiliario.
- Visualizar el mercado mediante mapas interactivos.
- Analizar indicadores de precio por metro cuadrado.
- Identificar comparables de mercado.
- Estimar el valor comercial de inmuebles mediante modelos AVM.
- Generar reportes automáticos de análisis de mercado.

---

# 3. Actores del Sistema

Los principales actores identificados son:

### Propietario de inmueble
Persona que desea conocer el valor aproximado de su propiedad.

### Avaluador profesional
Especialista que utiliza el sistema para obtener comparables y análisis de mercado.

### Agente inmobiliario
Usuario que analiza precios del mercado para comercialización de inmuebles.

### Inversionista inmobiliario
Usuario interesado en detectar oportunidades de inversión.

### Administrador del sistema
Usuario encargado de gestionar el sistema, usuarios y modelos.

---

# 4. Procesos del Negocio

El sistema contempla tres tipos de procesos.

---

## Procesos Estratégicos

- Definición de metodologías de valoración.
- Definición de políticas de datos.
- Gobernanza de modelos de machine learning.

---

## Procesos Misionales

- Captura de datos inmobiliarios.
- Procesamiento y limpieza de datos.
- Análisis del mercado inmobiliario.
- Generación de avalúos automatizados.
- Visualización del mercado.

---

## Procesos de Apoyo

- gestión de usuarios
- mantenimiento del sistema
- monitoreo de modelos
- soporte técnico

---

# 5. Requisitos Funcionales

## RF01 – Registro de usuario
El sistema debe permitir el registro de usuarios mediante correo electrónico.

---

## RF02 – Autenticación
El sistema debe permitir iniciar sesión mediante credenciales seguras.

---

## RF03 – Captura de datos inmobiliarios
El sistema debe capturar información de ofertas inmobiliarias desde portales web mediante técnicas de scraping.

---

## RF04 – Almacenamiento de datos
El sistema debe almacenar los datos capturados en una base de datos geoespacial.

---

## RF05 – Georreferenciación
El sistema debe asignar coordenadas geográficas a los inmuebles registrados.

---

## RF06 – Visualización del mercado
El sistema debe mostrar los inmuebles en un mapa interactivo.

---

## RF07 – Filtros de búsqueda
El sistema debe permitir filtrar inmuebles por:

- zona
- precio
- área
- tipo de inmueble
- número de habitaciones
- estrato

---

## RF08 – Cálculo de precio por metro cuadrado
El sistema debe calcular automáticamente el precio por metro cuadrado de cada inmueble.

---

## RF09 – Identificación de comparables
El sistema debe identificar comparables inmobiliarios similares al inmueble sujeto.

---

## RF10 – Generación de avalúo automatizado
El sistema debe estimar el valor comercial de un inmueble mediante modelos de Machine Learning.

---

## RF11 – Explicación del modelo
El sistema debe mostrar las variables que influyen en la estimación del valor.

---

## RF12 – Generación de reportes
El sistema debe generar reportes automáticos en formato PDF o Word.

---

## RF13 – Dashboard de mercado
El sistema debe mostrar indicadores del mercado inmobiliario:

- precio promedio por zona
- precio promedio por metro cuadrado
- tendencias del mercado

---

## RF14 – Administración del sistema
El sistema debe permitir a los administradores gestionar usuarios y modelos.

---

# 6. Requisitos No Funcionales

## RNF01 – Seguridad

El sistema debe proteger la información mediante autenticación segura y control de accesos.

---

## RNF02 – Rendimiento

El sistema debe responder a consultas en menos de 5 segundos.

---

## RNF03 – Escalabilidad

El sistema debe permitir la integración de nuevas fuentes de datos y expansión a nuevas ciudades.

---

## RNF04 – Usabilidad

El sistema debe ofrecer una interfaz clara y fácil de usar.

---

## RNF05 – Disponibilidad

El sistema debe tener una disponibilidad mínima del 99%.

---

## RNF06 – Explicabilidad

Los modelos de machine learning deben permitir explicar las variables que influyen en la estimación.

---

## RNF07 – Calidad de datos

El sistema debe detectar:

- datos incompletos
- duplicados
- valores atípicos

---

# 7. Reglas de Negocio

- El sistema generará **estimaciones automáticas de valor**, no avalúos periciales oficiales.
- El valor estimado será un **valor referencial de mercado**.
- El sistema mostrará un nivel de confianza en la estimación.
- Los comparables deben cumplir criterios mínimos de similitud.

---

# 8. Historias de Usuario

### HU01

Como propietario  
quiero conocer el valor aproximado de mi inmueble  
para tener una referencia de mercado.

---

### HU02

Como avaluador  
quiero encontrar comparables de mercado  
para respaldar mis avalúos.

---

### HU03

Como inversionista  
quiero analizar precios por zona  
para identificar oportunidades de inversión.

---

### HU04

Como agente inmobiliario  
quiero analizar el precio promedio por metro cuadrado  
para fijar precios competitivos.

---

# 9. Priorización Scrum

### Must Have

- captura de datos
- base de datos
- visualización en mapa
- cálculo de precio por m²
- modelo AVM básico

---

### Should Have

- comparables automáticos
- reportes PDF
- dashboard analítico

---

### Could Have

- API pública
- predicción de tendencia de precios
- alertas de inversión

---

# 10. Criterios de Aceptación

Un requisito se considera cumplido cuando:

- la funcionalidad está implementada
- se realizan pruebas satisfactorias
- el usuario puede ejecutar la función correctamente
- el sistema cumple con los requisitos definidos.

---

# 11. Trazabilidad

Los requisitos definidos en este documento se basan en:

- análisis del mercado inmobiliario
- documentos de investigación del proyecto
- evidencias del programa Tecnólogo ADSO
- necesidades identificadas mediante encuestas y análisis de usuarios.

---

# 12. Evolución del Sistema

El sistema podrá evolucionar para incluir:

- análisis de inversión inmobiliaria
- análisis de rentabilidad
- integración con datos catastrales
- expansión a nuevas ciudades
- integración con sistemas financieros