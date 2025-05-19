## 1. Comparación

Se utilizan operadores de comparación para filtrar registros en función de una relación entre columnas o valores.

**Operadores comunes:**
- `=` : Igual a  
- `<>` o `!=` : Distinto de  
- `<` : Menor que  
- `>` : Mayor que  
- `<=` : Menor o igual que  
- `>=` : Mayor o igual que  

**Ejemplo:**
```sql
SELECT * FROM empleados WHERE salario > 50000;
```

## 2. Pertenencia (`IN`)

La condición `IN` se utiliza para verificar si un valor se encuentra dentro de un conjunto definido de valores. Es útil cuando se desea comparar una columna con múltiples opciones posibles.

### 🔧 Sintaxis básica:

```sql
SELECT columnas
FROM tabla
WHERE columna IN (valor1, valor2, valor3, ...);
```

## 4. Rango (`BETWEEN`)

La condición `BETWEEN` se utiliza para filtrar registros que se encuentran **dentro de un intervalo**, incluyendo **los valores límite**.

### 🔧 Sintaxis básica:

```sql
SELECT columnas
FROM tabla
WHERE columna BETWEEN valor_inicial AND valor_final;
```

## 5. Nula (`IS NULL` / `IS NOT NULL`)

Las condiciones `IS NULL` y `IS NOT NULL` se utilizan para filtrar registros que **no tienen valor asignado** (es decir, son nulos) o que **sí tienen un valor**.

### 🔧 Sintaxis básica:

```sql
SELECT columnas
FROM tabla
WHERE columna IS NULL;

SELECT columnas
FROM tabla
WHERE columna IS NOT NULL;
```
