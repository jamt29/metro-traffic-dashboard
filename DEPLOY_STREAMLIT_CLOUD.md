# Despliegue del Dashboard en Streamlit Community Cloud

El dashboard es reproducible y se despliega en Streamlit Community Cloud (gratuito).

## 1. Preparar el repositorio (GitHub)

1. Crear un repositorio público en GitHub, p. ej. `metro-traffic-dashboard`.
2. Subir el contenido completo de la carpeta `01_Dashboard/` (mínimo: `app.py`, `requirements.txt`, `data/`, `README.md` y `.streamlit/`). La carpeta `data/` debe quedar al mismo nivel que `app.py`.
3. Verificar que `requirements.txt` contenga las dependencias (ya incluido).

## 2. Desplegar en Streamlit Cloud

1. Ir a https://share.streamlit.io e iniciar sesión con la cuenta de GitHub.
2. Clic en **New app**.
3. Seleccionar el repositorio, rama (`main`) y archivo principal `app.py`.
4. Clic en **Deploy**. La primera construcción tarda ~2–3 minutos.
5. Copiar la URL pública generada (formato `https://<usuario>-<repo>-<hash>.streamlit.app`).

## 3. Actualizar los entregables con el enlace

- Reemplazar el marcador `[URL a completar tras el despliegue]` en `README.md` y en la adenda
  (`docs/adenda_ieee_seccion_VB.docx` / `.pdf`) por la URL real.
- Si se desea, regenerar el PDF de la adenda desde Word tras el cambio.

## Notas

- Los datos (`data/Metro_Interstate_Traffic_Volume_clean.csv`) deben estar versionados en el repo;
  Streamlit Cloud no accede a archivos locales fuera del repo.
- `requirements.txt` fija las dependencias principales e incluye `statsmodels`, necesario para la línea de tendencia OLS de Plotly Express.
- Si falla la construcción, revisar los logs en la pestaña **Manage app** de Streamlit Cloud.
