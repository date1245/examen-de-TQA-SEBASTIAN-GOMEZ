# Análisis de caja blanca

## Código analizado
```python
def validar_compra(edad, cuenta_activa, saldo, monto):
    if edad < 18:
        return "Compra no permitida: edad"

    if not cuenta_activa:
        return "Compra no permitida: cuenta"

    if saldo >= monto and monto > 0:
        return "Compra aprobada"

    return "Compra rechazada"
```

## Decisiones y condiciones
| Decisión | Expresión | Condiciones simples |
|---|---|---|
| D1 | `edad < 18` | C1: `edad < 18` |
| D2 | `not cuenta_activa` | C2: `not cuenta_activa` |
| D3 | `saldo >= monto and monto > 0` | C3: `saldo >= monto`, C4: `monto > 0` |

Hay 3 decisiones, 4 condiciones simples y 4 sentencias `return` (una por cada salida).

## Criterio utilizado: cobertura de decisiones
Cada decisión debe tomar el resultado verdadero y el falso al menos una vez.

**Mínimo de casos: 4.** Las salidas verdaderas de D1 y D2 terminan la función, así que cada una necesita su propio caso. D3 necesita uno verdadero y otro falso, y ambos deben pasar antes por D1 falsa y D2 falsa.

## Casos diseñados
| Caso | edad | cuenta_activa | saldo | monto | Resultado esperado | Cubre |
|---|---|---|---|---|---|---|
| 1 | 17 | True | 100 | 50 | Compra no permitida: edad | D1 verdadera |
| 2 | 20 | False | 100 | 50 | Compra no permitida: cuenta | D1 falsa, D2 verdadera |
| 3 | 20 | True | 100 | 50 | Compra aprobada | D2 falsa, D3 verdadera |

## ¿Alcanzan los 3 casos?
No. Falta el resultado falso de D3, que es el único camino a `Compra rechazada`. Ajuste: agregar un cuarto caso.

| Caso | edad | cuenta_activa | saldo | monto | Resultado esperado | Cubre |
|---|---|---|---|---|---|---|
| 4 | 20 | True | 10 | 50 | Compra rechazada | D3 falsa |

Con los 4 casos se cubren los 4 `return` y las 3 decisiones en verdadero y falso.

## Comparación con otros criterios
- **Sentencias:** mínimo 4 casos, uno por cada `return`. Los mismos 4 casos lo cumplen.
- **Condiciones:** cada condición simple debe ser verdadera y falsa. Los casos 1 a 4 cubren C1, C2 y C3, pero C4 (`monto > 0`) nunca es falsa, porque Python no la evalúa cuando `saldo >= monto` es falso. Se necesita un quinto caso: `edad=20, cuenta_activa=True, saldo=100, monto=0` → Compra rechazada.
- Cobertura de decisiones no es lo mismo que cobertura de condiciones: D3 queda cubierta sin haber probado `monto > 0` en falso.
