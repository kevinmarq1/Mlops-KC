# 🧠 MLOps - Clasificador de Cáncer de Mama con FastAPI y MLflow

Este proyecto implementa una API de predicción de cáncer de mama basada en modelos de machine learning, desarrollada en un entorno MLOps. La solución combina el entrenamiento de modelos, registro automático con MLflow y despliegue mediante FastAPI. Adicionalmente, se integran modelos preentrenados de HuggingFace para tareas de NLP como análisis de sentimiento y resumen de texto.

---

## 🚀 Cómo usar este proyecto

1. Clona el repositorio y accede al directorio:

```bash
git clone https://github.com/tu-usuario/mlops-project.git
cd mlops-project
```

2. Crea y activa el entorno:

```bash
conda create -n mlops_env python=3.10
conda activate mlops_env
pip install -r requirements.txt
```

3. Inicia el servidor local:

```bash
uvicorn app.main:app --reload
```

4. Accede a la documentación interactiva de la API:

👉 http://127.0.0.1:8000/docs

## 🗂 Estructura del proyecto

Todo el proyecto está organizado con una arquitectura modular y clara, separando notebooks, scripts y la API:

```
mlops-project/
│
├── app/
│   ├── main.py
│   ├── schemas.py
│   └── utils/
│       └── ml_utils.py
│
├── notebooks/
│   ├── Practica_Despliegues_Alg_Kevin_Marquez.ipynb
│   └── latest_run_id.txt
│
├── mlruns/
│
├── requirements.txt
├── README.md
├── imagenes (capturas del api)

```

> Nota: se incluye la carpeta `mlruns/` válida y funcional para ejecutar la API sin necesidad de reentrenar.

---

## 📍 Endpoints disponibles

- `GET /`
- `GET /features`
- `POST /predict`
- `POST /summarize`
- `POST /sentiment`

---

## 🔧 Entrenamiento del modelo (opcional)

1. Abre el notebook:
```bash
Practica_Despliegues_Alg_Kevin_Marquez.ipynb
```

2. Entrena y registra el modelo.
3. Se guardará en `notebooks/` y se actualizará `latest_run_id.txt`.

---

## 🤖 Modelos utilizados

- `RandomForestClassifier`
- Hugging Face NLP:
  - `distilbert-base-uncased-finetuned-sst-2-english`

---

## ✍️ Autor

**Kevin Márquez**  
[@kevinmarqdrinks](https://www.instagram.com/kevinmarqdrinks)  
Proyecto para el bootcamp de Big Data y Machine Learning - KeepCoding
