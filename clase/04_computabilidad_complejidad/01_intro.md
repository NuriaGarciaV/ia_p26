---
title: "Introducción: Los Límites de lo Computable"
---

# Introducción: Los Límites de lo Computable

¿Hay cosas que una computadora nunca podrá hacer? ¿Sin importar cuánto tiempo le demos?

## Las Tres Grandes Preguntas

Cuando estudiamos computación, hay tres preguntas fundamentales que debemos hacernos:

### 1️⃣ ¿Qué podemos computar?

**La pregunta:** ¿Qué tipo de problemas puede resolver una computadora en principio?

**La respuesta corta:** Todo lo que una **Máquina de Turing** puede computar.

**La sorpresa:** Resulta que todos los modelos de computación razonables (Máquinas de Turing, funciones recursivas, λ-calculus, tu laptop, Python, JavaScript) son **equivalentes** en poder expresivo. Esto se llama la **Church-Turing Thesis**.

**Ejemplo:** Calcular $\pi$ hasta un millón de dígitos — computacionalmente posible (solo toma tiempo).

---

### 2️⃣ ¿Qué NO podemos computar?

**La pregunta:** ¿Hay problemas que ninguna computadora puede resolver, sin importar cuánto tiempo le demos?

**La respuesta sorprendente:** ¡SÍ! Hay problemas **indecidibles**.

**El ejemplo clásico:** El **Halting Problem**
- Pregunta: "¿Este programa eventualmente se detiene?"
- Resultado: **No existe** un programa que pueda responder esto para todos los casos

**Más sorprendente aún:** Muchos problemas prácticos son indecidibles:
- ¿Este código tiene un bug?
- ¿Estos dos programas hacen lo mismo?
- ¿Esta optimización siempre funciona?

---

### 3️⃣ ¿Qué tan rápido podemos computar?

**La pregunta:** Para problemas que SÍ podemos resolver, ¿cuánto tiempo toma?

**La respuesta:** Depende de la **clase de complejidad** del problema.

**Las clases principales:**
- **P** — problemas que se pueden resolver **eficientemente** (tiempo polinomial)
- **NP** — problemas cuyas soluciones se pueden **verificar** eficientemente
- **NP-completo** — los problemas "más difíciles" de NP

**El problema del millón:** ¿P = NP? (literalmente, hay $1,000,000 de premio)

**Ejemplo práctico:**
- Ordenar 1000 números — P (rápido: $O(n \log n)$)
- Problema del viajante con 1000 ciudades — NP-completo (probablemente exponencial)

---

## El Panorama Completo

Imagina todos los problemas posibles organizados en círculos concéntricos:

```
┌─────────────────────────────────────────┐
│  Todos los problemas posibles           │
│                                          │
│  ┌────────────────────────────────┐     │
│  │  Computables                   │     │
│  │  (eventualmente da respuesta)  │     │
│  │                                │     │
│  │  ┌──────────────────────┐      │     │
│  │  │  Decidibles          │      │     │
│  │  │  (siempre termina)   │      │     │
│  │  │                      │      │     │
│  │  │   ┌──────────┐       │      │     │
│  │  │   │    P     │       │      │     │
│  │  │   │ (rápido) │       │      │     │
│  │  │   └──────────┘       │      │     │
│  │  │       ↑              │      │     │
│  │  │      NP?             │      │     │
│  │  └──────────────────────┘      │     │
│  └────────────────────────────────┘     │
│                                          │
│  Fuera: No computables (ej: algunos     │
│  problemas sobre números reales)        │
└─────────────────────────────────────────┘
```

**Observaciones clave:**
- No todo es computable
- De lo computable, no todo es decidible (puede no terminar)
- De lo decidible, no todo es eficiente (puede tomar tiempo exponencial)

---

## ¿Por Qué Importa?

### Para Ciencias de la Computación
- Define **qué es posible** en principio
- Define **qué es práctico** en la realidad
- Nos dice cuándo **parar de buscar** el algoritmo perfecto

### Para Inteligencia Artificial
- Un agente de IA está limitado por estas barreras
- No podemos crear un "verificador universal de programas"
- Debemos usar **heurísticas** para problemas NP-completos

### Para Matemáticas y Lógica
- Los Teoremas de Gödel usan ideas similares al Halting Problem
- Muestran que hay **límites fundamentales** incluso en la lógica matemática
- Algunas verdades matemáticas son **verdaderas pero no demostrables**

### Para Filosofía
- ¿Qué significa "resolver" un problema?
- ¿Hay cosas que nunca podremos saber?
- ¿Los humanos pueden hacer más que las computadoras?

---

## Roadmap del Módulo

**Parte I: Fundamentos**
1. **Algoritmos y Turing** — El modelo de computación
2. **Computabilidad vs Decidibilidad** — Dos tipos de "resolver"

**Parte II: Límites**
3. **Halting Problem** — El límite fundamental
4. **Gödel** — Límites también en lógica/matemáticas

**Parte III: Eficiencia**
5. **Big-O** — Midiendo la velocidad
6. **P, NP, BPP** — Clases de complejidad
7. **P vs NP** — El problema abierto más importante

**Síntesis:** Conectando todo

---

## Una Advertencia

Este módulo trata sobre **límites y imposibilidad**. Puede ser philosophically unsettling:

- Descubrirás que hay preguntas que **nunca** podrás responder con código
- Aprenderás que algunos problemas **nunca** serán eficientes
- Verás que las matemáticas tienen **agujeros fundamentales**

Pero también es **liberador**:
- Sabrás cuándo parar de buscar un algoritmo perfecto
- Entenderás por qué algunas cosas requieren heurísticas
- Apreciarás la belleza de los límites fundamentales

---

**Siguiente:** [Algoritmos y Máquinas de Turing →](02_algoritmos_turing.md)
