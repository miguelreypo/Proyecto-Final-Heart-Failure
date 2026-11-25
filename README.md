# Proyecto final: Heart Failure Prediction Dataset

**Estudiante:** Luis Miguel Reyes Prado  
**Modalidad:** Individual  
**Asignatura:** Gestión de Datos  

## Objetivo
Analizar qué variables clínicas y demográficas presentan las asociaciones descriptivas más claras con la presencia de enfermedad cardíaca en 918 registros.

## Base de datos
- Fuente: https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction
- Archivo original: `heart.csv`
- Dimensiones: 918 filas × 12 columnas
- Contenido: 11 características clínicas y una variable objetivo binaria (`HeartDisease`).
- Origen: combinación de Cleveland, Hungarian, Switzerland, Long Beach VA y Statlog Heart.

## Archivos
```
.
├── README.md
├── heart.csv                         # Original sin modificar
├── heart_limpio.csv                  # Resultado reproducible
├── analisis_heart_failure.ipynb      # Código y explicación
├── Presentacion_Proyecto_Final.pptx  # Exposición
├── descripcion_base_datos.docx       # Documentación
├── guion_exposicion.md               # Guion aproximado de 8 minutos
└── figuras/                          # Seis visualizaciones
```

## Ejecución
1. Instalar Python 3.10+ y: `pip install pandas numpy matplotlib seaborn jupyter`.
2. Mantener `heart.csv` junto al notebook.
3. Abrir `analisis_heart_failure.ipynb` y ejecutar todas las celdas.

## Limpieza aplicada
- 0 nulos explícitos y 0 duplicados.
- 1 valor `RestingBP=0` imputado con mediana positiva.
- 172 valores `Cholesterol=0` imputados con mediana positiva por sexo y rango de edad.
- No se eliminan columnas.
- Se crean `AgeGroup` y `RiskProfile` para el análisis.

## Hallazgos principales
- Enfermedad registrada: 508/918 (55.3%).
- Angina de esfuerzo: 85.2% con enfermedad, contra 35.1% sin angina de esfuerzo.
- ST_Slope Flat: 82.8%; Up: 19.7%.
- Dolor ASY: 79.0% con enfermedad.

## GitHub
Por ser un trabajo individual, usar `main` como rama final del proyecto y una rama de trabajo `luis-miguel-reyes-prado`. Para esta segunda entrega, integrar la rama de trabajo a `main`, como pide el documento final. No modificar `heart.csv`.

```bash
git init
git add README.md
git commit -m "Inicializa repositorio"
git branch -M main
git checkout -b luis-miguel-reyes-prado
git add .
git commit -m "Agrega análisis final de enfermedad cardíaca"
git checkout main
git merge luis-miguel-reyes-prado
```

## Limitaciones
Este análisis es exploratorio, no causal ni diagnóstico. La muestra reúne conjuntos históricos y no representa necesariamente una población actual específica.
