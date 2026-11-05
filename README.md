# Metro Traffic — Dashboard Analítico

Dashboard interactivo sobre el dataset **Metro Interstate Traffic Volume** (UCI ML Repository),
que visualiza los resultados del pipeline de datos (Fases I–V) de la asignatura
**Análisis de Datos (UEES)**.

## Ejecución local

Desde esta carpeta (`01_Dashboard/`), ejecuta:

```bash
pip install -r requirements.txt
streamlit run app.py
```

El CSV se encuentra en `data/`, junto a la aplicación, por lo que esta carpeta puede probarse
localmente y publicarse como raíz de un repositorio de Streamlit Cloud.

Se abre en `http://localhost:8501`.

## Datos

- `data/Metro_Interstate_Traffic_Volume_clean.csv` — dataset limpio y transformado (40 575 filas × 16 variables).
- Origen: `Metro_Interstate_Traffic_Volume.csv.gz` (UCI). Pipeline documentado en los notebooks
  `01_Ingesta_Perfilado_EDA.ipynb` y `02_Limpieza_Transformacion_Auditoria.ipynb`.

## Estructura de la aplicación

```
01_Dashboard/
├── app.py
├── requirements.txt
├── README.md
├── DEPLOY_STREAMLIT_CLOUD.md
├── .streamlit/config.toml
└── data/
    └── Metro_Interstate_Traffic_Volume_clean.csv
```

## Lugar y fecha de entrega

San Salvador, miércoles 4 de noviembre de 2026

## Enlace interactivo / repositorio reproducible

- Repositorio (reproducible): https://github.com/DarrFun/metro-traffic-dashboard
- App en Streamlit Cloud: `[URL a completar tras el despliegue en Streamlit Community Cloud]`

Ver `DEPLOY_STREAMLIT_CLOUD.md` para los pasos del despliegue en la nube.

## Principios de diseño

- **Gramática de los Gráficos:** posición y longitud para comparaciones precisas; color solo con
  propósito funcional (azul = tráfico, naranja = temperatura, rojo = alerta).
- **Gestalt & Tufte:** máximo data-to-ink, sin chartjunk, bordes innecesarios ni gráficos 3D/circulares densos.
- **Shneiderman:** overview (KPIs) → zoom/filter (filtros globales sincronizados) → details-on-demand
  (tooltips, tabla de inspección, descarga).
- **Data Storytelling:** Diagnóstico → Patrones → Causa raíz → Recomendación.
