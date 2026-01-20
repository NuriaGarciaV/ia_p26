---
title: "Lógica Proposicional"
---

# Lógica Proposicional

El lenguaje más simple para representar conocimiento.

## ¿Qué es una Proposición?

Una **proposición** es una declaración que puede ser **verdadera** o **falsa**, pero no ambas.

| Declaración | ¿Es proposición? | Valor |
|-------------|------------------|-------|
| "Está lloviendo" | ✓ Sí | V o F |
| "2 + 2 = 4" | ✓ Sí | V |
| "¿Qué hora es?" | ✗ No | Pregunta |
| "¡Cierra la puerta!" | ✗ No | Imperativo |
| "x > 5" | ✗ No* | Depende de x |

*En lógica proposicional no hay variables. En FOL (lógica de primer orden) sí.

---

## Sintaxis de la Lógica Proposicional

La **sintaxis** define qué expresiones son "gramaticalmente correctas".

### Símbolos Proposicionales

Los átomos básicos son **símbolos proposicionales**:

| Símbolo | Interpretación típica |
|---------|----------------------|
| $P, Q, R, S$ | Proposiciones cualesquiera |
| $True$ | Siempre verdadero |
| $False$ | Siempre falso |

### Conectivos Lógicos

Los conectivos combinan proposiciones:

| Conectivo | Nombre | Símbolo | Lectura |
|-----------|--------|---------|---------|
| **Negación** | NOT | $\neg$ | "no P" |
| **Conjunción** | AND | $\land$ | "P y Q" |
| **Disyunción** | OR | $\lor$ | "P o Q" |
| **Implicación** | IF-THEN | $\rightarrow$ | "si P entonces Q" |
| **Bicondicional** | IFF | $\leftrightarrow$ | "P si y solo si Q" |

### Gramática Formal (BNF)

```
Sentencia → AtomicSentence | ComplexSentence
AtomicSentence → True | False | Symbol
Symbol → P | Q | R | ...
ComplexSentence → ¬ Sentencia
                | Sentencia ∧ Sentencia
                | Sentencia ∨ Sentencia
                | Sentencia → Sentencia
                | Sentencia ↔ Sentencia
                | ( Sentencia )
```

### Precedencia de Operadores

Del más alto al más bajo:

| Prioridad | Operador | Asociatividad |
|-----------|----------|---------------|
| 1 (más alta) | $\neg$ | — |
| 2 | $\land$ | Izquierda |
| 3 | $\lor$ | Izquierda |
| 4 | $\rightarrow$ | Derecha |
| 5 (más baja) | $\leftrightarrow$ | — |

**Ejemplo:**
$$\neg P \land Q \rightarrow R$$

Se parsea como:
$$((\neg P) \land Q) \rightarrow R$$

---

## Semántica de la Lógica Proposicional

La **semántica** define qué **significan** las expresiones — cuándo son verdaderas o falsas.

### Modelos e Interpretaciones

Un **modelo** $m$ es una asignación de valores de verdad a todos los símbolos proposicionales.

**Ejemplo:** Si tenemos símbolos $\{P, Q, R\}$:
- $m_1 = \{P=True, Q=True, R=False\}$
- $m_2 = \{P=False, Q=True, R=True\}$

Para $n$ símbolos, hay $2^n$ modelos posibles.

### Tablas de Verdad

Las tablas de verdad definen la semántica de cada conectivo:

#### Negación ($\neg$)

| $P$ | $\neg P$ |
|:---:|:--------:|
| T | F |
| F | T |

#### Conjunción ($\land$)

| $P$ | $Q$ | $P \land Q$ |
|:---:|:---:|:-----------:|
| T | T | **T** |
| T | F | F |
| F | T | F |
| F | F | F |

"Ambos deben ser verdaderos"

#### Disyunción ($\lor$)

| $P$ | $Q$ | $P \lor Q$ |
|:---:|:---:|:---------:|
| T | T | T |
| T | F | T |
| F | T | T |
| F | F | **F** |

"Al menos uno debe ser verdadero" (OR inclusivo)

#### Implicación ($\rightarrow$)

| $P$ | $Q$ | $P \rightarrow Q$ |
|:---:|:---:|:-----------------:|
| T | T | T |
| T | F | **F** |
| F | T | T |
| F | F | T |

**¡Importante!** La implicación es **verdadera por vacuidad** cuando el antecedente es falso.

:::example{title="Implicación Vacuamente Verdadera"}

"Si 2+2=5, entonces yo soy el Papa"

- $P$ = "2+2=5" = False
- $Q$ = "yo soy el Papa" = False

$P \rightarrow Q$ = **True** (¡la implicación es verdadera!)

**Intuición:** Una promesa no se rompe si la condición nunca se cumple.

"Si sacas 10, te compro un carro"
- Si sacas 10 y te compro → Cumplí ✓
- Si sacas 10 y NO te compro → Mentí ✗
- Si NO sacas 10 → No puedes acusarme de mentir ✓

:::

#### Bicondicional ($\leftrightarrow$)

| $P$ | $Q$ | $P \leftrightarrow Q$ |
|:---:|:---:|:---------------------:|
| T | T | **T** |
| T | F | F |
| F | T | F |
| F | F | **T** |

"Ambos tienen el mismo valor" (equivalencia)

---

## Evaluando Fórmulas

Para evaluar una fórmula en un modelo, aplicamos las tablas de verdad recursivamente.

:::example{title="Evaluación de Fórmula"}

Evalúa $(P \land Q) \rightarrow \neg R$ en el modelo $m = \{P=T, Q=T, R=F\}$

**Paso a paso:**

1. $P = T$, $Q = T$, $R = F$
2. $P \land Q = T \land T = T$
3. $\neg R = \neg F = T$
4. $(P \land Q) \rightarrow \neg R = T \rightarrow T = T$

**Resultado:** True

:::

### Tabla de Verdad Completa

Para una fórmula con $n$ variables, construimos una tabla con $2^n$ filas:

**Fórmula:** $(P \rightarrow Q) \land (\neg Q \rightarrow \neg P)$

| $P$ | $Q$ | $\neg P$ | $\neg Q$ | $P \rightarrow Q$ | $\neg Q \rightarrow \neg P$ | **Fórmula** |
|:---:|:---:|:--------:|:--------:|:-----------------:|:---------------------------:|:-----------:|
| T | T | F | F | T | T | **T** |
| T | F | F | T | F | F | **F** |
| F | T | T | F | T | T | **T** |
| F | F | T | T | T | T | **T** |

---

## Equivalencias Lógicas

Dos fórmulas son **lógicamente equivalentes** ($\equiv$) si tienen el mismo valor de verdad en **todos** los modelos.

### Equivalencias Fundamentales

#### Leyes de De Morgan

$$\neg (P \land Q) \equiv \neg P \lor \neg Q$$
$$\neg (P \lor Q) \equiv \neg P \land \neg Q$$

**Intuición:** "No ambos" = "al menos uno no"; "Ninguno" = "no el primero y no el segundo"

#### Implicación como Disyunción

$$P \rightarrow Q \equiv \neg P \lor Q$$

**Muy importante para resolución**

#### Contrapositiva

$$P \rightarrow Q \equiv \neg Q \rightarrow \neg P$$

"Si llueve, entonces la calle se moja" ≡ "Si la calle no está mojada, no llovió"

#### Doble Negación

$$\neg \neg P \equiv P$$

#### Conmutatividad

$$P \land Q \equiv Q \land P$$
$$P \lor Q \equiv Q \lor P$$

#### Asociatividad

$$(P \land Q) \land R \equiv P \land (Q \land R)$$
$$(P \lor Q) \lor R \equiv P \lor (Q \lor R)$$

#### Distributividad

$$P \land (Q \lor R) \equiv (P \land Q) \lor (P \land R)$$
$$P \lor (Q \land R) \equiv (P \lor Q) \land (P \lor R)$$

#### Bicondicional

$$P \leftrightarrow Q \equiv (P \rightarrow Q) \land (Q \rightarrow P)$$

---

## Formas Normales

Las **formas normales** son representaciones estandarizadas de fórmulas.

### Literal

Un **literal** es un símbolo proposicional o su negación:
- Literal positivo: $P$
- Literal negativo: $\neg P$

### Cláusula

Una **cláusula** es una disyunción de literales:
$$L_1 \lor L_2 \lor \cdots \lor L_n$$

**Ejemplo:** $P \lor \neg Q \lor R$

### Forma Normal Conjuntiva (CNF)

Una fórmula está en **CNF** si es una conjunción de cláusulas:
$$(L_{11} \lor \cdots \lor L_{1k}) \land (L_{21} \lor \cdots \lor L_{2m}) \land \cdots$$

**Ejemplo en CNF:**
$$(P \lor Q) \land (\neg P \lor R) \land (\neg Q \lor \neg R)$$

### Forma Normal Disyuntiva (DNF)

Una fórmula está en **DNF** si es una disyunción de conjunciones:
$$(L_{11} \land \cdots \land L_{1k}) \lor (L_{21} \land \cdots \land L_{2m}) \lor \cdots$$

**Ejemplo en DNF:**
$$(P \land Q) \lor (\neg P \land R) \lor (Q \land \neg R)$$

### Conversión a CNF

Algoritmo para convertir cualquier fórmula a CNF:

1. **Eliminar bicondicionales:** $\alpha \leftrightarrow \beta$ → $(\alpha \rightarrow \beta) \land (\beta \rightarrow \alpha)$
2. **Eliminar implicaciones:** $\alpha \rightarrow \beta$ → $\neg \alpha \lor \beta$
3. **Mover negaciones hacia adentro** (De Morgan):
   - $\neg(\alpha \land \beta)$ → $\neg \alpha \lor \neg \beta$
   - $\neg(\alpha \lor \beta)$ → $\neg \alpha \land \neg \beta$
   - $\neg \neg \alpha$ → $\alpha$
4. **Distribuir** $\lor$ sobre $\land$:
   - $\alpha \lor (\beta \land \gamma)$ → $(\alpha \lor \beta) \land (\alpha \lor \gamma)$

:::example{title="Conversión a CNF"}

Convertir: $P \rightarrow (Q \land R)$

**Paso 1:** No hay bicondicionales

**Paso 2:** Eliminar implicación
$$\neg P \lor (Q \land R)$$

**Paso 3:** Negaciones ya están bien

**Paso 4:** Distribuir $\lor$ sobre $\land$
$$(\neg P \lor Q) \land (\neg P \lor R)$$

**Resultado CNF:** $(\neg P \lor Q) \land (\neg P \lor R)$

:::

---

## Cláusulas de Horn

Una **cláusula de Horn** es una cláusula con **a lo más un literal positivo**.

| Tipo | Forma | Ejemplo |
|------|-------|---------|
| **Cláusula definida** | Exactamente 1 positivo | $\neg P \lor \neg Q \lor R$ |
| **Cláusula objetivo** | 0 positivos | $\neg P \lor \neg Q$ |
| **Hecho** | 1 positivo, 0 negativos | $P$ |

### Importancia de las Cláusulas de Horn

Las cláusulas definidas se pueden escribir como **reglas**:

$$\neg P \lor \neg Q \lor R \equiv (P \land Q) \rightarrow R$$

"Si P y Q, entonces R"

**Ventaja computacional:** La inferencia con cláusulas de Horn es **O(n)** en lugar de NP-completo.

---

## Ejercicios

:::exercise{title="Tabla de Verdad" difficulty="1"}

Construye la tabla de verdad para: $\neg P \lor (P \land Q)$

| $P$ | $Q$ | $\neg P$ | $P \land Q$ | $\neg P \lor (P \land Q)$ |
|:---:|:---:|:--------:|:-----------:|:------------------------:|
| T | T | ? | ? | ? |
| T | F | ? | ? | ? |
| F | T | ? | ? | ? |
| F | F | ? | ? | ? |

¿Qué observas sobre esta fórmula?

:::

<details>
<summary><strong>Ver Solución</strong></summary>

| $P$ | $Q$ | $\neg P$ | $P \land Q$ | $\neg P \lor (P \land Q)$ |
|:---:|:---:|:--------:|:-----------:|:------------------------:|
| T | T | F | T | **T** |
| T | F | F | F | **F** |
| F | T | T | F | **T** |
| F | F | T | F | **T** |

**Observación:** La fórmula es equivalente a $Q \lor \neg P$, o equivalentemente $P \rightarrow Q$.

Podemos verificar: ambas tienen el mismo patrón T, F, T, T.

</details>

---

:::exercise{title="Equivalencias" difficulty="2"}

Demuestra usando tablas de verdad que:

$$P \rightarrow Q \equiv \neg P \lor Q$$

:::

<details>
<summary><strong>Ver Solución</strong></summary>

| $P$ | $Q$ | $P \rightarrow Q$ | $\neg P$ | $\neg P \lor Q$ |
|:---:|:---:|:-----------------:|:--------:|:---------------:|
| T | T | T | F | T |
| T | F | F | F | F |
| F | T | T | T | T |
| F | F | T | T | T |

Las columnas $P \rightarrow Q$ y $\neg P \lor Q$ son idénticas, por lo tanto son **lógicamente equivalentes**.

</details>

---

:::exercise{title="Conversión a CNF" difficulty="2"}

Convierte a CNF: $(P \land Q) \rightarrow R$

:::

<details>
<summary><strong>Ver Solución</strong></summary>

**Paso 1:** Eliminar implicación
$$\neg(P \land Q) \lor R$$

**Paso 2:** Aplicar De Morgan
$$(\neg P \lor \neg Q) \lor R$$

**Paso 3:** Asociatividad (ya está en CNF)
$$\neg P \lor \neg Q \lor R$$

**Resultado:** Una sola cláusula: $(\neg P \lor \neg Q \lor R)$

**Nota:** Esta es una cláusula de Horn (un literal positivo).

</details>

---

:::exercise{title="Formalización" difficulty="2"}

Formaliza las siguientes afirmaciones en lógica proposicional:

1. "Si no estudias, reprobarás"
2. "Aprobarás si y solo si estudias o tienes suerte"
3. "No puedes tener la torta y comértela también"

Define claramente tus símbolos proposicionales.

:::

<details>
<summary><strong>Ver Solución</strong></summary>

**Símbolos:**
- $E$ = "Estudias"
- $A$ = "Apruebas"
- $S$ = "Tienes suerte"
- $T$ = "Tienes la torta"
- $C$ = "Te comes la torta"

**Formalizaciones:**

1. "Si no estudias, reprobarás" (reprobar = no aprobar)
   $$\neg E \rightarrow \neg A$$
   
   Equivalente (contrapositiva): $A \rightarrow E$ ("Si apruebas, estudiaste")

2. "Aprobarás si y solo si estudias o tienes suerte"
   $$A \leftrightarrow (E \lor S)$$

3. "No puedes tener la torta y comértela también"
   $$\neg(T \land C)$$
   
   Equivalente: $\neg T \lor \neg C$

</details>

---

:::exercise{title="Identificación de Formas" difficulty="1"}

Clasifica cada fórmula:

| Fórmula | ¿CNF? | ¿DNF? | ¿Horn? |
|---------|:-----:|:-----:|:------:|
| $(P \lor Q) \land (\neg P \lor R)$ | ? | ? | ? |
| $(P \land Q) \lor (R \land S)$ | ? | ? | ? |
| $\neg P \lor \neg Q \lor R$ | ? | ? | ? |
| $P \land Q \land R$ | ? | ? | ? |

:::

<details>
<summary><strong>Ver Solución</strong></summary>

| Fórmula | ¿CNF? | ¿DNF? | ¿Horn? |
|---------|:-----:|:-----:|:------:|
| $(P \lor Q) \land (\neg P \lor R)$ | ✓ Sí | ✗ No | ✗ No (2 positivos en cláusula 1) |
| $(P \land Q) \lor (R \land S)$ | ✗ No | ✓ Sí | N/A |
| $\neg P \lor \neg Q \lor R$ | ✓ Sí | ✗ No | ✓ Sí (1 positivo) |
| $P \land Q \land R$ | ✓ Sí (cada var es cláusula) | ✓ Sí (1 conjunción) | ✓ Sí (hechos) |

</details>

---

:::prompt{title="Practicar Lógica Proposicional" for="Claude/ChatGPT"}

Quiero practicar lógica proposicional. Por favor:

1. Dame 5 ejercicios de tablas de verdad con fórmulas de 2-3 variables
2. Dame 3 ejercicios de conversión a CNF
3. Dame 2 problemas de formalización (del mundo real a lógica)
4. Después de que intente resolverlos, dame retroalimentación detallada

Empieza con los ejercicios de tablas de verdad.

:::

---

## Puntos Clave

1. **Proposición** = declaración verdadera o falsa
2. **Sintaxis** = reglas gramaticales (qué expresiones son válidas)
3. **Semántica** = significado (cuándo son verdaderas)
4. **Conectivos**: $\neg, \land, \lor, \rightarrow, \leftrightarrow$
5. **Implicación** es verdadera cuando el antecedente es falso (vacuamente verdadera)
6. **Equivalencias** importantes: De Morgan, contrapositiva, $P \rightarrow Q \equiv \neg P \lor Q$
7. **CNF** = conjunción de cláusulas (importante para SAT)
8. **Cláusulas de Horn** permiten inferencia eficiente
