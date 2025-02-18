## **Diseño 1 - Errores y soluciones**

### **Errores encontrados:**
1. **Falta un identificador único en la clase `Espacio`**
   - Cada espacio debe tener un número o código único para diferenciarlo.
2. **No se incluye la capacidad del espacio**
   - Es importante saber cuántas personas pueden usar el espacio al mismo tiempo.
3. **`GestorReservas` no administra bien las reservas**
   - No está claro cómo se guarda la relación entre reservas y espacios.
4. **No hay un método para revisar si un espacio está libre antes de reservar**
   - El sistema debería verificar si un espacio está disponible antes de reservarlo.
5. **No hay una opción para cancelar una reserva**
   - No se puede liberar un espacio después de que alguien ya no lo necesite.

### **Solución sugerida:**
- Agregar un atributo `int id` en `Espacio` para darle un número único.
- Incluir `int capacidad` para definir cuántas personas pueden usar el espacio.
- Mejorar `GestorReservas` para guardar bien las reservas.
- Agregar un método `bool estaDisponible()` en `Espacio` para revisar si está libre.
- Incluir un método `void liberar()` para que un espacio vuelva a estar disponible.



## **Diseño 2 - Errores y soluciones**

Este diseño es **igual al Diseño 1**, por lo que tiene los mismos problemas y necesita las mismas soluciones.



## **Diseño 3 - Errores y soluciones**

### **Mejoras respecto a los anteriores:**
! Se agregó `capacidad` en `Espacio`.
! Se incluyeron métodos como `estaDisponible()`, `consultarTarifaHora()` y `liberar()`.
! Se cambió la forma en que `Reserva` maneja los espacios, haciéndolo más simple y seguro.

### **Errores aún presentes:**
1. **Falta un identificador único en `Espacio`**.
2. **No se especifica si `GestorReservas` actualiza la disponibilidad del espacio al reservarlo**.

### **Solución sugerida:**
- Agregar `int id` en `Espacio`.
- Modificar `realizarReserva()` en `GestorReservas` para que marque el espacio como reservado.
- Agregar un método `void cancelarReserva()` para liberar un espacio si la reserva se cancela.