# 🤖 Clasificador Automático de RAEE: Análisis de Regresión para la Evaluación de Proyectos

Este repositorio contiene la aplicación interactiva utilizada en el **Estudio de Mercado y Proyección Financiera** del proyecto "Clasificador Automático de Residuos de Aparatos Eléctricos y Electrónicos (RAEE)", siguiendo la metodología de **Gabriel Baca Urbina**.

La aplicación permite realizar un **Análisis de Regresión Lineal Simple** en tiempo real para determinar qué variable macroeconómica (Inflación, PIB, IPC) es el mejor predictor del precio de venta (Oferta y Demanda) del Clasificador RAEE, basándose en el coeficiente de determinación ($\mathbf{R^2}$).

---

## 📊 Metodología de Análisis

El objetivo es encontrar la relación lineal óptima ($\mathbf{P = a + bX}$) que mejor se ajusta a los datos históricos o proyectados del mercado.

El criterio de selección del modelo más robusto es el **Coeficiente de Determinación ($\mathbf{R^2}$)**:

* **Si $\mathbf{R^2} \rightarrow 1$:** El modelo es excelente; la variable $X$ (ej. PIB) explica casi toda la variación del Precio ($P$).
* **Si $\mathbf{R^2} \rightarrow 0$:** El modelo es débil; la variación del Precio no se explica por la variable $X$.

El modelo con el $\mathbf{R^2}$ más alto será el que se utilice para la proyección del precio de venta durante los 5 años del horizonte de evaluación financiera del proyecto.

---

## 🚀 Aplicación Interactiva (Demo)

El archivo principal (`regresion_unificada.html`) contiene toda la aplicación, incluyendo el CSS y JavaScript embebido.

### 🔗 Enlace a la Aplicación
[Inserta aquí el enlace de GitHub Pages: `https://[su-nombre-de-usuario].github.io/[nombre-del-repositorio]/regresion_unificada.html`]

### ⚙️ Instrucciones de Uso

1.  **Valores X (Global):** En la primera caja de texto (marcada en azul), ingrese los valores de la variable independiente ($\mathbf{X}$). Estos valores deben ser consistentes para las 6 regresiones.
    * *Ejemplo:* Si usa los períodos de tiempo: `1, 2, 3, 4, 5, 6`
    * *Ejemplo:* Si usa la Inflación histórica: `5.2, 6.1, 7.0, 5.5, 6.5, 7.5`

2.  **Valores Y (Precios):** En cada uno de los 6 modelos siguientes, ingrese los valores históricos o proyectados del Precio ($\mathbf{P}$) (Valores $\mathbf{Y}$). Asegúrese de que la cantidad de Valores Y sea **exactamente igual** a la cantidad de Valores X ingresados globalmente.

3.  **Análisis en Tiempo Real:** Al ingresar los datos, la aplicación automáticamente:
    * **Grafica** la nube de puntos.
    * **Calcula y dibuja** la Línea de Regresión ($\mathbf{P = a + bX}$).
    * **Muestra** la ecuación de regresión con la Ordenada al Origen ($a$) y la Pendiente ($b$) con 3 decimales.
    * **Muestra** el $\mathbf{R^2}$ (Coeficiente de Determinación) con 4 decimales.

---

## 🛠️ Estructura del Proyecto

El proyecto está diseñado para la máxima portabilidad:

* **`regresion_unificada.html`:** Contiene toda la lógica (HTML, CSS y JavaScript).
* **JavaScript:** Incluye funciones para el cálculo de la Regresión Lineal (mínimos cuadrados), la pendiente ($b$), la ordenada ($a$), y el $R^2$.
* **Librería de Gráficos:** Utiliza la librería **Chart.js** (cargada vía CDN) para renderizar las 6 gráficas de dispersión de manera dinámica.

---

## 📜 Autor

* **Autor:** Carlos L. Noriega M.
* **Proyecto:** Evaluación de Proyectos (225) - UNA Ingeniería de Sistemas
* **Lapso:** 2025-2
