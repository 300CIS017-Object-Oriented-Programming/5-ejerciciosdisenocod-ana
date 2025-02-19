DIAGRAMA 1 SOLUCIÓN

ERRORES:
Faltan atributos en espacio como el id único para cada espacio ni cuenta con un int capacidad máxima de los espacios 
falta un método que verifique si los espacios están disponibles o no  
los atributos del diagrama son públicos, cuando deberían ser privados 
la relación entre los espacios y reservas deberían ser más específicos, ya que en reserva se almacena un espacio* cuando debería ser una referencia única 
en el gestor de reservas falta un método para liberar las reservas
en el gestor de reservas para cancelar y realizar la reserva ambas reciben un objeto y no un id

SOLUCIÓN:
agregar los atributos int id y int capacidad en espacio 
agregar el método que verifique si un espacio está disponible con bool estaDisponible()
pasar los atributos de públicos a privados
cambiar la relación entre las reservas y los espacios con una referencia única con Espacio espacio
agregar un método para liberar la reserva como void liberarReserva(int reservaId)
en el gestor de reservas debería manejar identificadores únicos así realizarReserva(int espacioId, int duracion) y cancelarReserva(int reservaId)