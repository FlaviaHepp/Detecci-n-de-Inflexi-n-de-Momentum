# Detección de Inflexión de Momentum

Caídas Bruscas del RSI desde Sobrecompra

Este proyecto implementa una consulta SQL que identifica cambios abruptos en el momentum, detectando acciones cuyo RSI cae más de 10 puntos en un solo día luego de haber estado en zona de sobrecompra.

La señal apunta a capturar puntos de inflexión tempranos, antes de que la tendencia de precios se deteriore visiblemente.

## 🧠Idea central

- El momentum no se degrada siempre de forma gradual.

En muchos techos de mercado ocurre lo siguiente:
- el precio aún se sostiene
- los indicadores de tendencia siguen sanos
- pero el RSI colapsa de golpe
- Cuando el momentum se quiebra violentamente, el mercado suele estar cambiando de régimen.

## 🎯Valor de negocio

Identifica posibles techos locales

Útil para:
- salidas tempranas
- ajuste de stops
- estrategias contrarian
- Reduce drawdowns en fases de distribución

## 🗄️Estructura de datos esperada

- indicadores_tecnicos
- campo	descripción
- ticker_id	Identificador del activo
- fecha	Fecha
- rsi_14	RSI de 14 períodos

## ⚙️Lógica de la consulta

- Calcula el RSI del día actual y del día previo
- Mide el cambio diario de RSI

Filtra acciones que:
- venían de sobrecompra (RSI > 70)
- sufren una caída > 10 puntos en un solo día
- Ordena por la magnitud del colapso de momentum

## 🔎Interpretación de resultados

- Caída brusca del RSI → agotamiento de compradores
- Desde sobrecompra → distribución, no corrección menor

Suele preceder:
- rupturas de soporte
- cruces bajistas de medias
- aumento de volatilidad

## 🚀Posibles extensiones

- Confirmar con volumen decreciente
- Analizar persistencia post-evento
- Aplicar filtros por ADX o SMA
- Backtesting por activo y mercado

## 📝Notas finales

- No es señal automática de venta
- Es una alerta de cambio de carácter
- Funciona mejor en mercados extendidos

## 👤Autora
Flavia Hepp Proyecto de SQL aplicó un análisis de riesgo basado en eventos.
