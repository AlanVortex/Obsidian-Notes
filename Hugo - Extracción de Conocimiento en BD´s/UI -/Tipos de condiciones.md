# Condiciones en Pandas 

## 1. Comparación

Se utilizan operadores de comparación para filtrar registros en función de una relación entre columnas o valores.

**Operadores comunes:**
- `==` : Igual a  
- `!=` : Distinto de  
- `<` : Menor que  
- `>` : Mayor que  
- `<=` : Menor o igual que  
- `>=` : Mayor o igual que  

**Ejemplo en Pandas (Edad mayor a 40):**

```python
df_csv[df_csv["age"] > 40]
```

## 2. Pertenencia (`IN`)

La condición `IN` se utiliza para verificar si un valor se encuentra dentro de un conjunto definido de valores. Es útil cuando se desea comparar una columna con múltiples opciones posibles.

### 🧠 ¿Qué hace?
Filtra los registros cuya columna coincida con **cualquiera** de los valores dados.

---
### 🔧 Sintaxis:

```python
df_csv[df_csv["home"].isin(["NY", "GBR"])]
```

![[Pasted image 20250521192645.png]]

## 3. Rango (`BETWEEN`)

La condición `BETWEEN` se utiliza para filtrar registros que se encuentran **dentro de un intervalo**, incluyendo los **valores límite**.

---

### 🧠 ¿Qué hace?
Devuelve los registros donde el valor de una columna esté entre un **mínimo** y un **máximo** dado (inclusive).

---

### 🔧 Sintaxis:
```pandas
df_csv[df_csv["time"].between(200, 250)]
```

![[Pasted image 20250521192816.png]]

## 4. Nula (`IS NULL` / `IS NOT NULL`)

Estas condiciones se utilizan para identificar registros donde **existen o faltan valores** en una columna.

---

### 🧠 ¿Qué hace?
- `IS NULL`: filtra registros sin valor asignado en una columna (vacíos o nulos).
- `IS NOT NULL`: filtra registros donde sí hay un valor.

---

### 🔧 Sintaxis:

```pandas
df_csv[df_csv["time"].isnull()]       # IS NULL
df_csv[df_csv["time"].notnull()]     # IS NOT NULL
```

![[Pasted image 20250521193005.png]]