# ✨Detección de Inflexión de Momentum

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

***
📉 **De sobrecompra a alerta en 24 horas. ¿Cambio de tendencia en puerta?**

Hay momentos en el mercado donde todo parece fuerte…
hasta que deja de serlo de golpe.

⚡ Un patrón que me interesa במיוחד:

👉 Acciones con **RSI > 70 (sobrecompra)**
👉 Que caen **más de 10 puntos en un solo día**

---

🧠 ¿Qué significa esto?

No es solo una caída de indicador.
Es un posible **punto de inflexión en el momentum**.

💡 Porque cuando el RSI cae bruscamente desde sobrecompra:

* El impulso comprador pierde fuerza
* Aparecen vendedores agresivos
* Se debilita la continuidad de la tendencia

---

🚨 No siempre marca un reversal inmediato…
pero sí suele anticipar:

✔️ Correcciones de corto plazo
✔️ Falsos breakouts
✔️ Inicio de distribución

---

📊 En este análisis detecté automáticamente estos eventos para identificar activos donde el “sentimiento extremo” cambia de forma abrupta.

---

📉 Insight clave:
**El peligro no es cuando el mercado cae…
es cuando deja de subir con la misma fuerza.**

---

🔍 Entender estos cambios de momentum permite adelantarse, no reaccionar.

#Trading #Quant #DataScience #Momentum #RSI #AnálisisTécnico #Finanzas

