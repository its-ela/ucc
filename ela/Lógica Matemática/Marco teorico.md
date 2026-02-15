# 1. ¿Qué es razonar?

**Razonar** es pasar de unas afirmaciones (**premisas**) a otra afirmación (**conclusión**) siguiendo alguna regla.

Hay dos grandes formas de razonamiento:

## 🔹 Razonamiento deductivo

- Va de lo **general** a lo **particular**
    
- Si la forma es válida y las premisas son verdaderas, la conclusión **es necesaria**
    

Ejemplo simple:

> Todos los sensores revisados funcionan.  
> Este sensor fue revisado.  
> → Este sensor funciona.

Aquí no hay probabilidad: hay **necesidad lógica**.

👉 Los **Casos 1, 2, 3 y 4** se analizan **principalmente de forma deductiva**.

---

## 🔹 Razonamiento inductivo

- Va de lo **particular** a lo **general**
    
- La conclusión es **probable**, no necesaria
    

Ejemplo:

> Cada vez que el sistema falló, había problemas eléctricos.  
> → Probablemente los problemas eléctricos causan las fallas.

👉 El **Caso 4** mezcla inducción con deducción mal hecha.

---

# 2. ¿Qué es un silogismo?

Un **silogismo** es una estructura deductiva clásica con:

1. **Premisa mayor** (regla general)
    
2. **Premisa menor** (caso concreto)
    
3. **Conclusión**
    

Ejemplo canónico:

> Todos S son P  
> a es S  
> → a es P

En los ejercicios:

- “Todos los sensores fueron revisados” (Caso 2)
    
- “Si T o P, entonces A” (Caso 3)
    

son **premisas mayores**.

---

# 3. Qué significan los símbolos que usamos

Para formalizar razonamientos usamos símbolos lógicos.

|Símbolo|Significado|Ejemplo|
|---|---|---|
|→|“si… entonces”|F → E|
|∧|“y”|T ∧ P|
|∨|“o” (inclusiva)|T ∨ P|
|¬|“no”|¬A|
|∴|“por lo tanto”|∴ F|

Ejemplo (Caso 3):

> Si la temperatura es alta **o** la presión es alta, entonces hay alarma

(T∨P)→A(T ∨ P) → A(T∨P)→

---

# 4. Condición necesaria y condición suficiente

Esto es **clave para TODOS los ejercicios**.

## 🔹 Condición suficiente

Si se cumple, el efecto ocurre.

Ejemplo:

> Si hay temperatura alta, se activa la alarma  
> T → A

T es **suficiente** para A.

👉 Caso 3: **T** y **P** son condiciones suficientes.

---

## 🔹 Condición necesaria

Debe estar presente para que algo ocurra, pero no lo garantiza.

Ejemplo:

> Cada vez que hubo falla, había problemas eléctricos  
> F → E

E es **necesaria** para F, pero no suficiente.

👉 Casos 1 y 4 confunden esto.

---

# 5. Antecedente y consecuente

En una proposición:

A→BA → BA→B

- **A** = antecedente
    
- **B** = consecuente
    

Ejemplo (Caso 4):

> Si el sistema falla (**F**), hay problemas eléctricos (**E**)

F es el antecedente  
E es el consecuente

---

# 6. La falacia central que aparece (Casos 1 y 4)

## ❌ Afirmación del consecuente

Forma inválida:

`Si A → B B ∴ A`

Ejemplo (Caso 1):

> Si el sistema falla → sensor mal calibrado  
> Sensor mal calibrado  
> → el sistema falla ❌

Ejemplo (Caso 4):

> Si el sistema falla → problemas eléctricos  
> Hay problemas eléctricos  
> → el sistema fallará ❌

👉 El error: **tratar una condición necesaria como si fuera suficiente**.

---

# 7. Afirmaciones universales (“todos”)

Del **Caso 2**.

Frase:

> Todos los sensores fueron revisados

Forma silogística:

> Todo S es P

Regla:

- Una afirmación universal **se invalida con una sola excepción**
    

Ejemplo:

> 11 sensores revisados  
> 1 sensor no revisado  
> → “Todos” es falso

Esto explica la **pregunta 3 del Caso 2**.

---

# 8. Disyunción lógica (“o”)

Del **Caso 3**.

En lógica:

- “o” es **inclusiva**, no exclusiva
    

T∨PT ∨ PT∨P

Significa:

- T
    
- o P
    
- o ambos
    

Por eso:

- Si T y P son altas al mismo tiempo → la alarma **igual se activa**
    

Esto responde la **pregunta 3 del Caso 3**.

---

# 9. Correlación vs causalidad (Caso 4, pregunta 2)

Dos cosas pueden ocurrir juntas sin que una cause la otra.

Ejemplo del caso:

> Siempre que hubo fallas, hubo problemas eléctricos

Eso indica:

- correlación histórica
    
- no causalidad lógica
    

Error:

> Como hoy hay problemas eléctricos, el sistema fallará

Silogísticamente inválido porque:

- E puede ocurrir sin F
    

---

# 10. Conexión final: cómo leer todos los ejercicios

Cuando leas un ejercicio, pregúntate siempre:

1. ¿Es inductivo o deductivo?
    
2. ¿Hay un “si… entonces”?
    
3. ¿Se está afirmando el antecedente o el consecuente?
    
4. ¿Se usa “todos”, “algunos”, “o”?
    
5. ¿Se confunde causa con acompañamiento?
    

Si respondes eso, **todos los casos se resuelven solos**.

---

## 🧠 Cierre

Lo que descubrimos en estos ejercicios es esto:

> Muchos errores técnicos **no son de ingeniería**,  
> son errores **lógicos mal formalizados**.