## 🔹 1. Formalización silogística de la regla

Regla del sistema:

> **“Si la temperatura es alta o la presión es alta, se activa una alarma.”**

Definimos términos:

- **T** = la temperatura es alta
- **P** = la presión es alta
- **A** = la alarma se activa

Forma lógica:

> **Si T o P, entonces A**

En lógica proposicional clásica:

(T∨P)→A

En clave silogística operacional:

- **T** es causa suficiente
- **P** es causa suficiente
- Basta **una** para obtener **A**

![[Pasted image 20260209222734.png]]

## 2️⃣ Pregunta 1: Dos situaciones distintas en las que la alarma se active

Aquí usamos **modus ponens disyuntivo** (razonamiento válido).

### 🔹 Situación 1

- Premisa mayor:
    
    > Si T o P, entonces A
    
- Premisa menor:
    
    > T
    
- Conclusión:
    
    > A
    

👉 La alarma se activa **aunque la presión sea normal**.

---

### 🔹 Situación 2

- Premisa mayor:
    
    > Si T o P, entonces A
    
- Premisa menor:
    
    > P
    
- Conclusión:
    
    > A
    

👉 La alarma se activa **aunque la temperatura sea normal**.

Ambos casos son **silogísticamente válidos**.

---

## 3️⃣ Pregunta 2: Situación en la que la alarma no se active

Para negar la conclusión (**¬A**), desde la regla debemos negar **toda** la condición suficiente.

Aplicamos la contraposición:

¬A→(¬T∧¬P)

Silogísticamente:

- La temperatura **no** es alta
- La presión **no** es alta

Entonces:

> No se activa la alarma.

⚠️ Importante:  
No basta con que **una** no sea alta; deben fallar **ambas**.

---

## 4️⃣ Pregunta 3: ¿Qué ocurre si la temperatura y la presión son altas al mismo tiempo?

Desde la silogística:

- Premisa mayor:
    
    > Si T o P, entonces A
    
- Premisa menor:
    
    > T y P
    

Dado que **T ∧ P implica T ∨ P**, se cumple la condición.

Conclusión:

👉 **La alarma se activa**, exactamente igual que en los otros casos.

No se “activa más”, ni “dos veces”.  
La regla es **disyuntiva inclusiva**, no exclusiva.

---

## 🧠 Cierre silogístico

Este caso muestra tres cosas clave:

1. **“O” es inclusiva** en lógica clásica (no excluye que ambas ocurran).
2. Cada disyunto es **condición suficiente**.
3. La única forma de negar el efecto es negar **todos** los disyuntos.