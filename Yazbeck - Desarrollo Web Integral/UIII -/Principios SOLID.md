## 🟣 S - Single Responsibility Principle (SRP)

> **Una clase debe tener una única razón para cambiar.**

Cada clase debe encargarse de una sola funcionalidad o responsabilidad dentro del sistema.  
Si una clase tiene más de una responsabilidad, puede provocar problemas cuando se modifique.

**Ejemplo:**  
Una clase que genere reportes **no se debe encargar** de imprimirlos.

---

## 🟣 O - Open/Closed Principle (OCP)

> **El software debe estar abierto para extensión, pero cerrado para modificación.**

Deberías poder añadir nuevas funcionalidades al sistema sin tener que modificar el código existente,  
lo cual ayuda a evitar errores y bugs.

**Ejemplo:**  
Puedes usar **herencia o interfaces** para extender funcionalidades sin cambiar la clase base.

---

## 🟣 L - Liskov Substitution Principle (LSP)

> **Las subclases deben poder ser usadas en lugar de sus clases base sin alterar el funcionamiento del programa.**

Si una subclase rompe el comportamiento esperado de su clase padre, está violando este principio.

**Ejemplo:**  
Si `Ave` tiene un método `volar()`, entonces una subclase `Pingüino` que no puede volar  
**no debería heredar de** `Ave`.

---

## 🟣 I - Interface Segregation Principle (ISP)

> **Una clase no debe verse forzada a implementar interfaces que no utiliza.**

Es preferible tener muchas interfaces pequeñas y específicas, en lugar de una sola interfaz grande y general.

**Ejemplo:**  
No obligues a una clase `Impresora3D` a implementar métodos de una interfaz `Impresora`  
como `imprimirDocumento()`, si solo imprime objetos tridimensionales.

---

## 🟣 D - Dependency Inversion Principle (DIP)

> **Las clases de alto nivel no deben depender de clases de bajo nivel, sino de abstracciones.**

En lugar de que una clase utilice directamente otra clase concreta, debe depender de interfaces o clases abstractas.

**Ejemplo:**  
Una clase `FacturaService` no debería crear internamente una instancia de `PDFGenerator`,  
sino depender de una interfaz `IGeneradorDeReportes`.

---

