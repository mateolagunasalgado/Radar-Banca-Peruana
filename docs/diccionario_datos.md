# Diccionario de Datos

A. FUENTES

Reporte: Balance General
Código: B-2201
Periodicidad: Mensual
Unidad: Miles de soles
Hoja: 1
Fila inicial de datos:
Columnas que se usan: Provisiones para créditos directos, Patrimonio, Total Activo

--------------------------------------------------

Reporte: Estado de Ganancias y Pérdidas
Código: B-2201
Periodicidad: Mensual
Unidad: Miles de soles
Hoja: 2
Fila inicial de datos:
Columnas que se usan: Resultado neto del ejercicio

--------------------------------------------------

Reporte: Indicadores Financieros
Código: B-2401
Periodicidad: Mensual
Unidad: Porcentaje
Hoja: 3
Fila inicial de datos:
Columnas que se usan: Ratio de Capital Global, Créditos Atrasados / Créditos Directos, Provisiones / Créditos Atrasados, ROE, ROA y Eficiencia

--------------------------------------------------

Reporte: Créditos Directos según Situación
Código: B-2315
Periodicidad: Mensual
Unidad: Miles de soles
Hoja: Única
Fila inicial de datos: 9
Columnas que se usan: Vigentes, Reestructurados, Refinanciados, Vencidos, Cobranza Judicial, Total Créditos Directos

--------------------------------------------------

B. BANCOS

ID Banco: BCP
Nombre actual: B. de Crédito del Perú (con sucursales en el exterior)
Nombres históricos:
Desde/Hasta:
Notas:

ID Banco: BBVA
Nombre actual: B. BBVA Perú
Nombres históricos: B. Continental
Desde/Hasta: Cambio entre 2018 y 2019 (a confirmar periodo exacto)
Notas: Mismo banco

ID Banco: SCOTIA
Nombre actual: Scotiabank Perú
Nombres históricos:
Desde/Hasta:
Notas:

ID Banco: IBK
Nombre actual: Interbank
Nombres históricos:
Desde/Hasta:
Notas:

ID Banco: MIBANCO
Nombre actual: Mibanco
Nombres históricos:
Desde/Hasta:
Notas:

ID Banco: BANBIF
Nombre actual: B. Interamericano de Finanzas
Nombres históricos:
Desde/Hasta:
Notas:

--------------------------------------------------

C. RATIOS

Ratio: Morosidad
Fórmula: (Vencidos + Cobranza Judicial) / Total Créditos Directos
Fuente: B-2315
Validación: Morosidad publicada en Indicadores Financieros

Ratio: Cartera de alto riesgo
Fórmula: (Vencidos + Cobranza Judicial + Refinanciados) / Total Créditos Directos
Fuente: B-2315
Validación: Cartera de alto riesgo publicada por SBS

Ratio: Cobertura
Fórmula: Provisiones para créditos directos / (Vencidos + Cobranza Judicial)
Fuente: B-2201 y B-2315
Validación: Provisiones / Créditos Atrasados

Ratio: ROE
Fórmula: Utilidad neta anualizada / Patrimonio promedio
Fuente: Estado de Ganancias y Pérdidas + Balance General
Validación: ROE publicado

Ratio: ROA
Fórmula: Utilidad neta anualizada / Activo promedio
Fuente: Estado de Ganancias y Pérdidas + Balance General
Validación: ROA publicado

Ratio: Capital Global
Fórmula: Dato directo
Fuente: Indicadores Financieros
Validación: No se calcula

Ratio: Eficiencia
Fórmula: Dato directo
Fuente: Indicadores Financieros
Validación: No se calcula

--------------------------------------------------

D. REGLAS DE CÁLCULO

¿El Estado de Ganancias y Pérdidas viene acumulado?
Resultado:
Observaciones:

¿Cómo se calcula el patrimonio promedio?
Resultado:
Promedio entre el patrimonio del período actual y el patrimonio de diciembre del año anterior.

Observaciones:
Patrimonio promedio = (Patrimonio actual + Patrimonio diciembre del año anterior) / 2

Esta definición reproduce mejor el ROE publicado por la SBS que el promedio con el trimestre anterior.

¿Cómo se calcula el activo promedio?
Resultado:
Promedio entre el activo del período actual y el activo de diciembre del año anterior.

Observaciones:
Activo promedio = (Activo actual + Activo diciembre del año anterior) / 2

Esta definición sigue la metodología SBS utilizada para los indicadores anualizados.

¿Qué hacer con Total Banca Múltiple?
Resultado: Excluir de la tabla de bancos.
Observaciones: Utilizar únicamente como validación.

¿Usar consolidado o separar MN y ME?
Resultado: Utilizar el total consolidado
Observaciones:
Balance General y Estado de Ganancias y Pérdidas contienen columnas MN, ME y TOTAL.
Para la versión 1 del proyecto se trabajará con los valores consolidados
(TOTAL) en lugar de separar MN y ME

--------------------------------------------------

E. PREGUNTAS ABIERTAS

- ¿En qué periodo exacto cambió B. Continental a B. BBVA Perú?
Estado: Pendiente

- ¿El Estado de Ganancias y Pérdidas viene acumulado durante el año?
Resultado: Sí.

Observaciones:
BBVA Perú 2025:
Marzo = 534,614
Junio = 1,107,167
Septiembre = 1,830,739
Diciembre = 2,390,979

La utilidad aumenta de forma acumulativa durante el año.
Por lo tanto, el Estado de Ganancias y Pérdidas se considera acumulado.

- ¿Qué definición de patrimonio promedio coincide mejor con el ROE publicado?
Estado: Pendiente

- ¿Qué definición de activo promedio coincide mejor con el ROA publicado?
Estado: Pendiente

- Validación de morosidad:

BBVA Perú - Diciembre 2025

Cálculo propio:
(Vencidos + Cobranza Judicial) / Total Créditos Directos
= (754,264 + 1,885,585) / 81,713,612
= 3.23%

Morosidad publicada por SBS:
3.23%

Resultado:
Coincide exactamente.
La fórmula de morosidad queda validada.