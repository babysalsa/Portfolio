# HR Analytics: Predicción y Reducción de Rotación de Personal

**Autor:** Samuel Hernández Estrada  
**Herramientas:** Python (pandas, matplotlib, seaborn), Jupyter Notebook  
**Dataset:** IBM HR Analytics Employee Attrition & Performance (Kaggle)

---

## 🎯 Objetivo del Proyecto

Identificar los factores críticos que causan rotación de personal (attrition) y desarrollar recomendaciones basadas en datos para reducir la pérdida de talento en 30%, generando ahorros de $1M+ anualmente.

---

## 📊 Dataset

- **Fuente:** [Kaggle - IBM HR Analytics](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)
- **Tamaño:** 1,470 empleados × 35 variables
- **Variables clave:** Salario, Departamento, OverTime, Satisfacción, Años en la empresa

---

## 🔍 Metodología

### 1. **Análisis Exploratorio (EDA)**
- Limpieza de datos (0 valores nulos)
- Distribución de attrition: 16.1% rotación (237 empleados)
- Análisis por departamento, salario y horas extra

### 2. **Identificación de Factores de Riesgo**
- Correlaciones con attrition
- Análisis multivariado (Departamento × Salario × OverTime)
- Segmentación de perfiles de alto riesgo

### 3. **Modelado de Impacto**
- Cuantificación de costos de rotación ($15K/empleado)
- Proyección de ROI de intervenciones
- Definición de KPIs de éxito

---

## 🚨 Hallazgos Clave

### 1️⃣ **Sales en Crisis: 20.6% de Rotación**
- **92 empleados** renunciaron en Sales (vs 13.8% en R&D)
- Impacto: **+28% más pérdida** que otros departamentos

![Rotación por Departamento](visualizations/grafica_2_attrition_departamento.png)

---

### 2️⃣ **Salario: Factor Crítico (-42.7%)**
- Empleados que renuncian ganan **$2,046 menos/mes** ($4,787 vs $6,833)
- Pérdida anual por empleado: **-$24,548**

![Salario vs Attrition](visualizations/grafica_3_salario_attrition.png)

---

### 3️⃣ **OverTime = 3x Más Rotación**
- Sin horas extra: **10.4%** rotación
- Con horas extra: **30.5%** rotación (+193%)

![OverTime Impact](visualizations/grafica_4_overtime_attrition.png)

---

### 4️⃣ **Perfil de Alto Riesgo Identificado**

**Criterios:** Sales + Salario <$5K + OverTime

| Métrica | Valor |
|---------|-------|
| Empleados en riesgo | 45 |
| Tasa de rotación | **46.7%** |
| Incremento vs promedio | **+190%** |

![Análisis Combinado](visualizations/grafica_5_departamento_overtime.png)

---

### 5️⃣ **Matriz de Correlaciones**

**Top 3 factores que aumentan rotación:**
1. OverTime (+0.246)
2. Distancia al trabajo (+0.078)
3. Número de empresas previas (+0.043)

**Top 3 factores que reducen rotación:**
1. Salario mensual (-0.160)
2. Experiencia total (-0.170)
3. Años en rol actual (-0.161)

![Heatmap](visualizations/grafica_6_heatmap_correlaciones.png)

---

## 💡 Recomendaciones de Negocio

### ✅ **1. Ajuste Salarial en Sales (ROI: 98%)**
- **Acción:** Aumentar salarios <$5K a mínimo $6K/mes
- **Inversión:** $45K/mes ($540K/año)
- **Retorno:** Reducir 21 renuncias = ahorro $315K
- **Payback:** 2.8 meses

### ✅ **2. Eliminar OverTime Obligatorio**
- **Acción:** Contratar 15-20 empleados adicionales en Sales
- **Costo:** $300K/año
- **Beneficio:** Reducir rotación de 30.5% a 15% en grupo OverTime
- **Ahorro:** $1.4M vs pérdida actual

### ✅ **3. Programa de Retención Integral**
- Bonos trimestrales por permanencia
- Plan de carrera (promociones cada 18 meses)
- Work-life balance: máximo 45 hrs/semana

---

## 📈 Impacto Proyectado

| Métrica | Antes | Después | Mejora |
|---------|-------|---------|--------|
| **Rotación General** | 16.1% | <12% | -25% |
| **Rotación Sales** | 20.6% | <15% | -27% |
| **Costo Anual** | $3.6M | $2.5M | **-$1.1M** |
| **ROI Inversión** | - | 98% | - |

---

## 🛠️ Tecnologías Utilizadas
```python
pandas         # Limpieza y análisis de datos
numpy          # Cálculos estadísticos
matplotlib     # Visualizaciones
seaborn        # Gráficos avanzados (heatmaps, boxplots)
```

---

## 📁 Estructura del Repositorio
```
proyecto2-hr-analytics/
├── data/                    # Dataset original
├── notebooks/               # Jupyter Notebook con análisis
├── visualizations/          # Gráficas generadas
├── README.md               # Este archivo
└── requirements.txt        # Dependencias Python
```

---

## 🚀 Cómo Reproducir el Análisis

1. **Clonar el repositorio:**
```bash
git clone https://github.com/tu-usuario/proyecto2-hr-analytics.git
cd proyecto2-hr-analytics
```

2. **Instalar dependencias:**
```bash
pip install -r requirements.txt
```

3. **Ejecutar notebook:**
```bash
jupyter notebook notebooks/analisis_hr_attrition.ipynb
```

---

## 📧 Contacto

**Samuel Hernández Estrada**  
📧 Samuel.Hernandez.Est@gmail.com  
📱 (442) 753-9090  
🔗 [LinkedIn](#) | [GitHub](#)

---

## 📚 Referencias

- Dataset: [Kaggle - IBM HR Analytics](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)
- Benchmark rotación: SHRM 2024 Employee Turnover Report
- Costo de reemplazo: Society for Human Resource Management (15K-30K USD/empleado)
