classDiagram
    class Ciudadano {
	    -int id
        -string nombre
        -string telefono
        -int puntosAcumulados
        +void registrarEntrega(Material, double peso)
        +int consultarPuntos()
    }
    class Empleado {
	    -int id
        -string nombre
        +void registrarMaterial(Ciudadano, Material, double peso)
    }
    class Material {
        -string tipo
        -float puntosPorKg
        +float calcularPuntos(float peso)
    }
    class Canje {
	    +Ciudadano* buscarCiudadanoPorId(int id)
        -int puntosAcumulados
        +registrarCanje()
    }
class SistemaReciclaje {
        -list<Ciudadano> ciudadanos
        -list<Empleado> empleados
        -list<Material> materiales
        +void registrarCiudadano(Ciudadano)
        +void registrarEmpleado(Empleado)
        +void agregarMaterial(Material)
        +Ciudadano* buscarCiudadano(int id)
	    +registrarCanje()
    }
    Ciudadano "1" --o "*" Material
    Empleado "1" --o "*" Material
    SistemaReciclaje "1" --o "*" Ciudadano
    SistemaReciclaje "1" --o "*" Empleado
    SistemaReciclaje "1" --o "*" Material
    Ciudadano "1" --o "*" Canje