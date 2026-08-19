# Algoritmo de Aprobación de Crédito

```text
INICIO
  ENTRADA: ingresos, deuda_actual, score

  // Paso 1: Validar ingresos mínimos
  SI ingresos < 1000 ENTONCES
    RETORNAR "Rechazado: Ingresos insuficientes"
  FIN SI

  // Paso 2: Calcular capacidad de pago
  capacidad = (ingresos * 0.4) - deuda_actual
  SI capacidad <= 0 ENTONCES
    RETORNAR "Rechazado: Capacidad de pago agotada"
  FIN SI

  // Paso 3: Revisar score crediticio
  SI score >= 650 ENTONCES
    RETORNAR "Crédito Aprobado"
  MAS SINO
    RETORNAR "Rechazado: Score bajo"
  FIN SI
FIN
