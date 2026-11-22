# Mall Customers: Segmentación de clientes con K-Means

Gestión de Proyectos de Datos · Evaluación Parcial N°5 · Parte A (datos y modelo)
Integrantes: Antonella Aedo · Carolina Aguirre · Javier Albornoz

Implementa las fases 2 a 4 de CRISP-DM del plan del EP3: calidad de datos, preparación y modelado. El modelo usa solo `Annual Income` y `Spending Score`; Gender, Age, Education y Marital Status quedan fuera del entrenamiento.

## Contenido

| Archivo | Descripción |
|---|---|
| `Parte_A_Segmentacion_KMeans.ipynb` | Notebook con todo el flujo, ya ejecutado |
| `Mall Customers.xlsx` | Muestra de datos entregada por el cliente (confidencial, ver nota) |
| `Informe.docx` | Sección de la Parte A del informe |
| `requirements.txt` | Librerías necesarias |
| `outputs/` | Resultados: calidad de datos (E2), selección de k, fichas de perfil, segmentos por cliente, gráficos y registro de la ejecución (E3, E4) |

## Nota sobre confidencialidad de los datos

Los datos corresponden a una muestra entregada por el cliente y son confidenciales: en un proyecto real no deben publicarse ni difundirse fuera del equipo. Se incluyen en este repositorio únicamente para efectos de la evaluación académica.

## Cómo ejecutarlo

```
pip install -r requirements.txt
jupyter notebook Parte_A_Segmentacion_KMeans.ipynb
```

El notebook lee `Mall Customers.xlsx` desde su misma carpeta (variable `RUTA_DATOS`) y escribe los resultados en `outputs/`. Si se mueve a otra carpeta del proyecto, basta con ajustar `RUTA_DATOS`. La semilla es fija (`42`), así que los resultados se reproducen.

## Resultados

- 200 clientes, sin nulos ni duplicados.
- k = 5: silueta 0,555 y segmento más pequeño de 11 % (cumple RNF04).
- Segmentos de 22 a 81 clientes.
- `outputs/E3_segmentos_clientes.csv` entrega `CustomerID` y `Segmento` para la auditoría de equidad.
