# 🛰️ Mapeo Móvil para Inventario Vial Rural - Colombia

![GNSS](https://img.shields.io/badge/GNSS--RTK-Submétrico-blue?style=for-the-badge)
![ArcGIS](https://img.shields.io/badge/ArcGIS_Pro-2C7AC3?style=for-the-badge&logo=arcgis&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)


<img width="880" height="1184" alt="2nJOjAZGrzPVdl8y12-bb" src="https://github.com/user-attachments/assets/c2a98dc7-014b-4343-9da4-966bc09dacfa" />


> Sistema de bajo costo para inventario georreferenciado de vías terciarias mediante GNSS-N-TRIP + Video 4K

---

## 🎯 Resumen

**Primera implementación documentada en Colombia** de mapeo móvil accesible para vías rurales. Sistema integrado GNSS + video georreferenciado que reduce costos en **60%** y tiempo en **600%** vs. métodos tradicionales, manteniendo precisión centimétrica (±1m).

### 📊 Resultados - Piloto La Palma, Cundinamarca
- **114.5 km** inventariados en **39 días**
- **416 propiedades** viales caracterizadas
- **106 obras de drenaje** + **34 sitios críticos** georreferenciados
- **Precisión**: ±1m horizontal, cumple Resolución 412/2020 del Ministerio de Transporte 

---

## 🔬 Problema → Solución

### Problema
Colombia tiene **142,284 km** de vías terciarias (68% de la red nacional):
- ❌ 60% en mal estado
- ❌ Sin inventario actualizado
- ❌ Métodos tradicionales: lentos (4-5h/tramo), costosos, inconsistentes
- ❌ Sistemas LIDAR comerciales: prohibitivamente caros

### Solución
**Sistema vehicular** que integra:
- Receptor GNSS-RTK (correcciones N-TRIP en tiempo real)
- Cámara 4K sincronizada temporalmente
- Software GIS especializado (Horus + ArcGIS Pro + Python)
- Metodología estandarizada (SINC-compliant)

---

## 🛠️ Stack Tecnológico

**Hardware:**
- Receptor GNSS Smart Delta (dual-frequency)
- Cámara 4K + IMU
- Montaje vehicular custom

**Software:**
- **ArcGIS Pro** + **QGIS**: Procesamiento GIS
- **Horus Suite**: Sincronización GNSS-video
- **Python**: Automatización (arcpy, cálculos geométricos)

**Precisión:** ±1m horizontal | ±2m vertical | 20-30 km/día

---

## 📐 Metodología (5 Fases - 39 días)

```
1. PLANIFICACIÓN (3d)     → Equipos, rutas, parámetros
2. CAPTURA CAMPO (8d)     → 20-30 km/día, monitoreo RTK
3. POST-PROCESAMIENTO (15d) → GNSS + video + etiquetado
4. CONTROL CALIDAD (10d)   → Topología, atributos, validación
5. ENTREGA (3d)           → Geodatabase + mapas + dashboard
```

### Capas Generadas (SINC-Compliant)

| Capa | Tipo | Cantidad | Descripción |
|------|------|----------|-------------|
| EJES | Línea | 29 | Geometría red vial |
| PROPIEDADES | Línea | 416 | Tipo terreno, pendiente, superficie, estado |
| SITIOSCRITICOS | Punto | 34 | Hundimientos, pérdida calzada (severidad 1-4) |
| OBRASDRENAJE | Punto | 106 | Alcantarillas, box culverts, canales |
| PUENTES | Punto | 6 | Estructuras mayores |
| FOTOEJE | Punto | 588 | Registro fotográfico cada 200m |
| PRS | Punto | 133 | Puntos referencia cada 1km |

---


## 📊 Resultados Cuantitativos

### Eficiencia vs. Métodos Tradicionales

| Métrica | Tradicional | Mapeo Móvil | Mejora |
|---------|-------------|-------------|--------|
| **Tiempo** | 4-5 h/tramo | 20-30 km/día | **600% más rápido** |
| **Costo** | $50M COP | $20M COP | **60% reducción** |
| **Precisión** | ±5m | ±1m | **5x mejor** |
| **Personal** | 4-5 personas | 2 personas | **50% menos** |

### Hallazgos La Palma

**Tipo Terreno:** Montañoso 45% | Ondulado 35% | Plano 20%  
**Superficie:** Afirmado 78% | Pavimento 15% | Tierra 7%  
**Estado:** Regular 52% | Bueno 28% | Malo 20%

---

## 📁 Estructura del Proyecto

```
mobile-mapping-rural-roads/
│
├── data/
│   ├── shapefiles/              # 8 capas SINC
│
├── maps/
│   ├── RED_VIAL_GENERAL.pdf
│   ├── SITIOS_CRITICOS.pdf
│   └── dashboard/
│
├── scripts/
│   └── python/
│       ├── shift_coordinates.py
│       ├── calculate_slopes.py
│       └── topological_validation.py
│
├── docs/
│   ├── MONOGRAFIA_74pag.pdf
│   └── PRESENTACION.pdf
│
└── README.md
```

---

## 🎓 Habilidades Demostradas

**Técnicas:**
- ✅ GNSS-RTK Surveying (N-TRIP corrections)
- ✅ Mobile Mapping Systems (hardware + software integration)
- ✅ Advanced GIS (ArcGIS Pro, QGIS, Python scripting)
- ✅ Geodatabase Design (topología, dominios, relaciones)
- ✅ Geospatial Analysis (validación, control de calidad)
- ✅ Remote Sensing (video georreferenciado)

**Metodológicas:**
- ✅ Research Design (problema, objetivos, metodología científica)
- ✅ Field Work Planning (logística, equipos, protocolos)
- ✅ Data Processing Pipelines (ETL automatizado)
- ✅ Quality Control (ISO standards, validación topológica)
- ✅ Technical Documentation (monografía académica)

---

## 🌍 Impacto y Escalabilidad

**Impacto Social:**
- Mejora conectividad rural en 142,284 km potenciales
- Facilita transporte agrícola, acceso a servicios
- Prioriza inversión en infraestructura crítica

**Escalabilidad Nacional:**
- Ahorro proyectado: **$42,000M COP** (60% vs. tradicional)
- Aplicable a 1,103 municipios con red terciaria
- Enfoque: Municipios PDET (territorios rurales prioritarios)

---

## 👥 Equipo

**Autores:** Aarón Mateo Tocora Jiménez, Cristián David Espíndola Rincón  
**Director:** Ing. Wilmar Darío Fernández Gómez  
**Institución:** Universidad Distrital Francisco José de Caldas  
**Grupo de investigación:** Infraestructura Sostenible  
📍 Bogotá, Colombia

---

## 📖 Documentación

- 🎤 [Presentación](https://gamma.app/docs/Metodologia-de-Mapeo-Movil-para-Inventario-Vial-Rural-1msd8n0fjkpzld4?mode=doc)
- 🌐 [Dashboard Interactivo]([DASHBOARD_LA_PALMA_ARCGIS_ONLINE](https://www.arcgis.com/apps/dashboards/f1946c760ee34d2a9dd63442c593cfdb))
- 🗺️ [Repositorio Mapas](https://udistritaleduco-my.sharepoint.com/personal/amtocoraj_udistrital_edu_co/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Famtocoraj%5Fudistrital%5Fedu%5Fco%2FDocuments%2FSALIDAS%5FGR%C3%81FICAS%5FMETODOLOG%C3%8DA%5FMAPEO%5FM%C3%93VIL%5FINVENTARIO%5FVIAL%5FRURAL&ga=1)

---

## 📄 Licencia

**Creative Commons BY-NC-SA 4.0**  
✅ Uso académico libre | ❌ Uso comercial requiere autorización

---

## 🙏 Agradecimientos

Alcaldía de La Palma, Cundinamarca | Universidad Distrital Franciso José de Caldas | Comunidades rurales | Ing. Wilmar Fernández

---

**⭐ Metodología innovadora que puede transformar la gestión vial rural en Colombia**
