# Dataset de clientes – NivelUp Store (tienda de videojuegos)

Dataset **sintético** creado con fines académicos para el Producto Académico N.° 3 del curso **Inteligencia de Negocios** (periodo 2026-20).

**NivelUp Store** es una empresa **ficticia**: una cadena peruana que vende videojuegos, consolas, accesorios, coleccionables y suscripciones por tienda física, web y app. Los datos **no corresponden a personas reales**.

## Desafío de negocio

NivelUp Store no sabe cómo agrupar a sus clientes para ofrecerles promociones personalizadas ni qué factores hacen que un cliente compre después de visitar su web.

- **Segmentación de clientes** (aprendizaje no supervisado – K-means)
- **Predicción de compra tras la visita web** (aprendizaje supervisado – regresión logística / árbol de decisión)

## Archivos

| Archivo | Descripción |
|---|---|
| `dataset_clientes_nivelup.csv` | Dataset en CSV (UTF-8, separador coma) |
| `Dataset_NivelUp_Videojuegos.xlsx` | Mismo dataset en Excel, con hojas *Diccionario* y *Léeme* |

- **Registros:** 5 025 filas (incluye 25 duplicadas a propósito)
- **Columnas:** 21
- **Fecha de corte:** 25/11/2026

## Diccionario de datos

| Columna | Tipo | Descripción |
|---|---|---|
| ID_Cliente | Texto | Código único del cliente |
| Genero | Texto | Masculino / Femenino |
| Edad | Número | Edad en años |
| Region | Texto | Región del Perú |
| Canal_Preferido | Texto | Tienda física / Web / App |
| Plataforma_Favorita | Texto | PlayStation / Xbox / Nintendo Switch / PC |
| Genero_Juego_Favorito | Texto | Acción, Shooter, RPG, Aventura, Deportes, Carreras, Estrategia |
| Categoria_Producto_Favorita | Texto | Videojuegos, Consolas, Accesorios, Coleccionables, Suscripciones y tarjetas |
| Monto_Compra_Promedio | Número (S/) | Ticket promedio por compra |
| Frecuencia_Compra | Número | Compras en los últimos 12 meses |
| Ultima_Compra_Dias | Número | Días desde la última compra (recencia) |
| Antiguedad_Meses | Número | Meses como cliente |
| Miembro_Fidelidad | Sí/No | Pertenece al programa de puntos |
| Uso_Cupon_Ultima_Compra | Sí/No | Usó cupón en su última compra |
| Visito_Web_Ultimos_30_Dias | Sí/No | Visitó la web/app en los últimos 30 días |
| Paginas_Vistas | Número | Páginas vistas en la última visita |
| Tiempo_Web_Min | Número | Minutos en la web en la última visita |
| Agrego_Al_Carrito | Sí/No | Agregó un producto al carrito |
| Recibio_Email_Promo | Sí/No | Recibió el correo promocional del mes |
| **Realizo_Compra** | 0/1 | **Variable objetivo:** compró tras su visita a la web |
| Fecha_Registro_Datos | Fecha | Fecha de corte de la extracción |

## Calidad de datos

El dataset incluye **problemas de calidad intencionales** para practicar el preprocesamiento: valores vacíos en `Edad` y `Region`, edades imposibles, texto inconsistente en `Region` y `Genero`, montos atípicos y filas duplicadas.

## Uso en Python

```python
import pandas as pd
url = "https://raw.githubusercontent.com/<usuario>/<repositorio>/main/dataset_clientes_nivelup.csv"
df = pd.read_csv(url)
```

## Licencia

Datos sintéticos de libre uso con fines educativos.
