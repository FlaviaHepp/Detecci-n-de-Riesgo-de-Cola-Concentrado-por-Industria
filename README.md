# 🏭Detección de Riesgo de Cola Concentrado por Industria

Kurtosis Industrial y Volatilidad Extrema

Este proyecto implementa una consulta SQL que identifica industrias con una concentración elevada de riesgo de cola, midiendo la kurtosis promedio de los retornos en el corto plazo.

La señal apunta a detectar segmentos del mercado donde los movimientos extremos no son eventos aislados, sino una característica estructural.

## 🧠Idea central

No todo el riesgo es visible a través de la volatilidad estándar.

Algunas industrias:
- muestran retornos “tranquilos” la mayor parte del tiempo
- pero concentran shocks extremos
- con pérdidas o ganancias abruptas

La kurtosis permite ver ese riesgo oculto que la varianza ignora.

## ⚠️Valor de negocio

Identifica riesgo sistémico sectorial

Útil para:
- control de exposición
- asignación de capital
- stress testing

Ayuda a anticipar eventos extremos no lineales

## 🗄️Estructura de datos esperada

- tickers
- campo	descripción
- ticker_id	Identificador del activo
- industria	Industria a la que pertenece
- indicadores_tecnicos
- campo	descripción
- ticker_id	Identificador
- fecha	Fecha
- kurtosis	Kurtosis de retornos

## ⚙️Lógica de la consulta

- Analiza el último mes de datos
- Calcula la kurtosis promedio por industria

Filtra industrias con:
- kurtosis significativamente elevada (ej. > 4)
- Ordena por mayor concentración de riesgo extremo

## 🔎Interpretación de resultados

- Kurtosis alta → retornos extremos frecuentes
- Concentración industrial → riesgo no diversificado

Implica:
- alta sensibilidad a eventos
- shocks regulatorios o tecnológicos
- colapsos o rallies violentos

## 🚀Posibles extensiones

- Comparar contra kurtosis del mercado total
- Analizar rolling windows
- Combinar con volatilidad implícita
- Crear un tail risk score por industria

## 📝Notas finales

- Métrica clave para gestión de riesgo avanzada
- No es señal de trading direccional
- Fundamental para portafolios multi-industria

## 👤Autora
Flavia Hepp Proyecto de SQL aplicó un análisis de riesgo basado en eventos.
