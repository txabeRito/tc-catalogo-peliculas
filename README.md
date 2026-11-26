# Catálogo de películas · Team Challenge

> Renombrad este fichero a `README.md` y completad las partes entre `<...>`.

**Equipo 1:** Agustín Roberto Olivera, Alejandro Serrano Molina, Daniel Ruiz Chaverri, Roberto Soteres Muñoz, Sergio Fernández Quintela.

Catálogo de películas enriquecido a partir del dataset MovieLens: análisis con Pandas, sinopsis y web oficial desde la API de TMDB, y sinopsis en español generadas con Gemini.

## Reparto de funciones

| Persona | Rol | Notebook / tarea |
|---|---|---|
| Daniel | Responsable de repo y datos | 01_ingesta_limpieza |
| Alejandro | Analista de datos | 02_analisis |
| Roberto | Integración con APIs | 03_tmdb |
| Agustín | IA generativa | 04_gemini |
| Sergio | Preguntas y cierre | 05_bonus_y_cierre |

## Instalación

```bash
git clone <https://github.com/txabeRito/tc-catalogo-peliculas.git>
cd <tc-catalogo-peliculas>
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env            # y rellenad las claves
```

## Claves necesarias

| Variable | Dónde se obtiene |
|---|---|
| `TMDB_READ_ACCESS_TOKEN` o `TMDB_API_KEY` | themoviedb.org → Settings → API |
| `GEMINI_API_KEY` | aistudio.google.com |

## Ejecución

Ejecutad los notebooks **en este orden** (cada uno genera un CSV en `data/processed/` que usa el siguiente):

1. `01_ingesta_limpieza.ipynb` → `movies_clean.csv`
2. `02_analisis.ipynb`
3. `03_tmdb.ipynb` → `movies10.csv`
4. `04_gemini.ipynb` → `movies10_es.csv`

## Resultados principales

- Destacamos la importancia de un buen orden de trabajo en GitHub y con los compañeros, y así poder sacar mucho más rápido el trabajo. 

- Se hizo evidente la importancia de trabajar con roles divididos y bien organizados y pensar el código o lo que estemos haciendo de esa forma (dejando descripción y contexto de lo que hicimos y por qué). Esto hizo mucho más productivo el challenge.

- Para conseguir el objetivo, fue importante que entre tareas, por ejemplo la 2 y la 3, hubiera un buen “contrato” para saber qué datos van a pasar de un lado a otro, y así poder trabajar en paralelo.
