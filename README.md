# Prueba técnica — Científico de Datos

En el siguiente repositorio se almacena el manejo de archivos y versiones relacionados al reto técnico para el puesto de científico de datos.

## Contexto

Solución analítica para estimar la probabilidad de fraude en reclamaciones de seguros de vida, a partir de una base de 12.776 reclamaciones de 3.621 asegurados distintos (2000-2026).

## Estructura del repositorio

- docs/ → instrucciones del reto, presentación final
- notebooks/ → notebook con todo el análisis, limpieza, modelado
- README.md

## Flujo del proyecto

1. Exploración y entendimiento del negocio
2. Limpieza de datos: variables irrelevantes, redundantes y con riesgo de fuga de información
3. Ingeniería de variables (feature engineering): 5 variables nuevas construidas a partir del historial y las fechas del siniestro
4. Modelado: se entrenaron y compararon 3 modelos
   - Árbol de decisión
   - Regresión logística
   - CatBoost
5. Interpretación de resultados y perfiles de riesgo
6. Arquitectura conceptual de scoring en producción

## Modelos y resultados

| Modelo | Recall (fraude) | Precisión (fraude) | F1 | AUC |
|---|---|---|---|---|
| Árbol de decisión | 76.7% | 86.4% | 0.81 | 0.79 |
| Regresión logística | 82.0% | 72.4% | 0.77 | 0.81 |
| CatBoost | 90.0% | 81.4% | 0.85 | 0.88 |

**Recomendación:** regresión logística como insumo interpretable para el negocio, CatBoost como motor de producción.

## Presentación final

La sustentación completa (contexto, hallazgos, modelo recomendado y arquitectura) está disponible en `docs/`.

## Autor

Sebastián Castaño Zuluaga