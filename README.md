# Escenarios de Cambio Climatico en los Oceònos con CMIP6

## Fase 1: Definición del Estudio

### 1.1 Objetivos
1. Evaluar los cambios proyectados en variables oceánicas clave en el contexto del cambio climático.
2. Analizar la variabilidad de las regiones clave del océano (Niño 3.4, Niño 1+2, Atlántico Tropical).
3. Determinar los impactos potenciales en Sudamérica, incluyendo la corriente de Humboldt y los ecosistemas marinos.

### 1.2 Alcance
- **Modelos**:
  - MPI-ESM1-2-LR: Resolución baja, buen desempeño en simulaciones globales.
  - NorESM2-MM: Multimodelo de Noruega, detallado en acoplamiento océano-atmósfera.
- **Escenario**: SSP5-8.5 (alto impacto climático).
- **Regiones**:
  - Pacífico Tropical
  - Atlántico Tropical
  - Corriente de Humboldt

## Fase 2: Preparación de Datos

### 2.1 Identificación de Variables
Variables de interés seleccionadas:
- `tos`: Temperatura superficial del mar.
- `so`: Salinidad superficial.
- `uo`, `vo`: Componentes zonal y meridional de la corriente oceánica.
- `ph`: pH oceánico (acidificación).

### 2.2 Descarga de Datos
- **Fuente**: ESGF (Earth System Grid Federation).
- **Resolución temporal**: Datos mensuales.
- **Resolución espacial**:
  - MPI-ESM1-2-LR: ~1.875° x 1.875°.
  - NorESM2-MM: ~1.0° x 1.0°.
- **Período**:
  - 1980-2014 (histórico).
  - 2020-2100 (proyección).
- **Organización**:
  - Carpetas estructuradas por modelo y variable.

## Fase 3: Procesamiento de Datos

### 3.1 Definición de Regiones
Extracción de datos para:
1. **Niño 3.4**: 5°N-5°S, 120°W-170°W.
2. **Niño 1+2**: 0°-10°S, 90°W-80°W.
3. **Atlántico Tropical Norte**: 0°-20°N, 60°W-30°W.
4. **Atlántico Sur**: 0°-20°S, 50°W-20°W.
5. **Corriente de Humboldt**: 10°S-40°S, 120°W-80°W.

### 3.2 Cálculo de Anomalías
- **Base climatológica**: 1980-2014.
- **Fórmula**: `Anomalía = Dato Actual - Media Histórica`.
- **Herramientas recomendadas**:
  - Python: `xarray`, `numpy`.
  - CDO: Para cálculo rápido de promedios y anomalías.

### 3.3 Series Temporales y Tendencias
- Calcular series temporales para cada región y variable.
- Identificar tendencias significativas mediante regresiones lineales: `y = mx + b`.

## Fase 4: Visualización

### 4.1 Mapas de Variables
- Generar mapas de anomalías para `tos`, `so` y `ph`.
- Comparar resultados de MPI-ESM1-2-LR y NorESM2-MM.

### 4.2 Series Temporales
- Crear gráficos para Niño 3.4, Niño 1+2 y Atlántico Tropical.
- Comparar entre modelos.

### 4.3 Comparación de Modelos
- Resaltar similitudes y diferencias entre modelos.
- Identificar regiones con mayor incertidumbre.

## Fase 5: Impactos en Sudamérica

### 5.1 Relación con Clima Regional
- Relacionar variaciones de Niño 3.4 y Niño 1+2 con:
  - Anomalías de precipitación en Perú, Brasil y Argentina.
  - Frecuencia de eventos extremos (sequías, inundaciones).

### 5.2 Impactos en Biodiversidad y Pesquerías
- Evaluar impactos en la Corriente de Humboldt (variabilidad térmica y salina).
- Analizar el efecto de la acidificación en ecosistemas marinos.

## Fase 6: Comparación de Escenarios

### 6.1 Evaluación del Escenario SSP5-8.5
- Identificar cambios extremos en comparación con el histórico.
- Evaluar impactos proyectados hacia el 2100.

### 6.2 Incertidumbre entre Modelos
- Determinar qué modelo proyecta mayores cambios.
- Identificar regiones con mayor dispersión entre simulaciones.

## Fase 7: Comunicación de Resultados

### 7.1 Reportes Científicos
- Incluir gráficos y mapas para Sudamérica.
- Resaltar diferencias entre MPI-ESM1-2-LR y NorESM2-MM.

### 7.2 Presentaciones
- Preparar resultados para audiencias científicas y políticas.
- Proponer acciones basadas en los hallazgos.

---

## Herramientas y Recomendaciones
1. **Python**:
   - Paquetes: `xarray`, `numpy`, `matplotlib`, `cartopy`.
   - Uso: Extracción de regiones y cálculo de anomalías.
2. **CDO**:
   - Funciones: Remapeo, cálculo de promedios y tendencias.
3. **Panoply**:
   - Visualización rápida de datos NetCDF.

