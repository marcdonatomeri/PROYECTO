# 📊 Análisis de la Demanda de Lenguajes de Programación

Proyecto de **web scraping y análisis de datos** que estudia la relación entre la **popularidad** de los lenguajes de programación y su **demanda laboral** real, combinando datos de tres fuentes distintas.

## 🎯 Objetivo

Responder preguntas como: *¿los lenguajes más populares son también los más demandados en el mercado laboral?* Para ello se recopilan, cruzan y visualizan datos de popularidad, ofertas de empleo y actividad en repositorios.

## 🗂️ Fuentes de datos

| Script | Fuente | Qué obtiene |
|---|---|---|
| `TIOBE_scraper.py` | [TIOBE Index](https://www.tiobe.com/tiobe-index/) (scraping con BeautifulSoup) | Ranking de popularidad de lenguajes |
| `API_Adzuna.py` | [API de Adzuna](https://developer.adzuna.com/) | Número de ofertas de empleo por lenguaje |
| `API_GitHub.py` | [API de GitHub](https://docs.github.com/rest) | Estadísticas de repositorios por lenguaje |
| `analisis.py` | — | Cruza los tres datasets y genera las visualizaciones |

## 📁 Estructura

```
.
├── TIOBE_scraper.py     # Scraping del índice TIOBE
├── API_Adzuna.py        # Consulta de ofertas de empleo (Adzuna)
├── API_GitHub.py        # Consulta de estadísticas de GitHub
├── analisis.py          # Análisis y gráficos comparativos
├── data/                # CSVs generados (tiobe, adzuna, github)
├── Graficos/            # Gráficos resultantes
├── Memoria.docx         # Memoria del proyecto
└── Presentacion proyecto ATD.pdf
```

## 🚀 Uso

1. Instala las dependencias:
   ```bash
   pip install requests beautifulsoup4 pandas matplotlib
   ```

2. Configura tus credenciales en los scripts (no se incluyen en el repositorio):
   - `API_Adzuna.py`: `API_ID` y `API_KEY` de Adzuna.
   - `API_GitHub.py`: `GITHUB_TOKEN` (token personal de GitHub, opcional pero recomendado para evitar límites de peticiones).

3. Ejecuta los scripts en orden (TIOBE genera la lista base de lenguajes):
   ```bash
   python TIOBE_scraper.py
   python API_Adzuna.py
   python API_GitHub.py
   python analisis.py
   ```

## 🛠️ Tecnologías

- **Python** — requests, BeautifulSoup, pandas, matplotlib
- **APIs** — Adzuna, GitHub
- **Web scraping** — TIOBE Index

---
> ⚠️ Recuerda no subir tus claves de API. Configúralas localmente en los scripts antes de ejecutarlos.
