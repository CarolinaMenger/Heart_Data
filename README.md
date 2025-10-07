🫀 Análisis de Factores de Riesgo para Enfermedades Cardiovasculares
Este proyecto explora un conjunto de datos clínicos de 70.000 pacientes para identificar patrones asociados a enfermedades cardiovasculares. Se aplican técnicas de limpieza, visualización, modelado predictivo y simulación de API externa para enriquecer el análisis y validar hipótesis epidemiológicas.

📁 Estructura del proyecto
- EDA_Cardiovascular.ipynb: notebook principal con todo el análisis
- README.md: documentación del proyecto
- /data: carpeta sugerida para almacenar el dataset original (heart_data.csv)

📊 Dataset utilizado
• 	Fuente: Kaggle - Exploring Risk Factors for Cardiovascular Disease
• 	Variables: edad, género, altura, peso, presión arterial, colesterol, glucosa, hábitos de salud y diagnóstico de enfermedad cardiovascular ()

🔍 Objetivos del análisis
• 	Identificar variables asociadas a la presencia de enfermedad cardiovascular
• 	Validar hipótesis clínicas mediante visualizaciones
• 	Entrenar modelos predictivos para estimar riesgo
• 	Simular una API externa para comparar resultados con datos poblacionales

🧪 Modelos entrenados
|  |  |  |  | 
|  |  |  |  | 
|  |  |  |  | 


- Se utilizó SelectKBest para seleccionar las 8 variables más relevantes
- Se comparó la importancia de variables entre ambos modelos
- Se visualizó la matriz de confusión y el reporte de clasificación
  
📈 Visualizaciones destacadas
- Boxplots y KDE para presión arterial, edad, colesterol y glucosa
- Gráficos de barras para actividad física, género y hábitos
- Scatterplot multivariable: edad vs presión vs colesterol vs diagnóstico
- Comparación visual de importancia de variables entre modelos

🌐 Simulación de API externa
Se creó una función que simula una API REST, devolviendo la prevalencia estimada de enfermedad cardiovascular según edad y género. Esta simulación permite contrastar los resultados del modelo con estimaciones epidemiológicas regionales.
def api_prevalencia_cardio(edad, genero):
    # Simulación basada en datos OPS/OMS
    if edad < 40:
        base = 0.05
    elif edad < 60:
        base = 0.15
    else:
        base = 0.30
    return round(base * (1.1 if genero == 2 else 0.9), 3)

🧠 Conclusiones
- La presión arterial sistólica, la edad y el colesterol son los principales factores asociados a la enfermedad cardiovascular.
- La actividad física muestra un efecto protector, aunque moderado.
- El modelo XGBoost superó a Random Forest en precisión y sensibilidad.
- La simulación de API externa refuerza la validez del análisis al alinearse con datos poblacionales.

🛠️ Tecnologías utilizadas
- Python (pandas, numpy, seaborn, matplotlib, scikit-learn, xgboost)
- Google Colab
- GitHub

📌 Cómo usar este proyecto
- Cloná el repositorio:
git clone https://github.com/tu_usuario/EDA_Cardiovascular.git
- Abrí el notebook en Google Colab o Jupyter
- Asegurate de tener el archivo heart_data.csv en la ruta correspondiente
- Ejecutá las celdas para reproducir el análisis

👩‍💻 Autoría
Proyecto desarrollado por Carolina, consultora en procesos y analítica de datos, especializada en ERPs, SQL y asistentes inteligentes.
Este trabajo combina exploración técnica, visión clínica y enfoque modular para entregar un análisis robusto y aplicable.









