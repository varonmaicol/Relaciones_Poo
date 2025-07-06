# 🧩 Superclases en Programación Orientada a Objetos (POO)

En Programación Orientada a Objetos (POO), una **superclase** (también llamada clase padre o clase base) es una clase que **proporciona atributos y métodos comunes** a otras clases que heredan de ella.

---

## 🧠 ¿Qué es una superclase?

> Una **superclase** define comportamientos y propiedades generales que pueden ser reutilizados por múltiples **subclases**.

- Contiene **atributos comunes**.
- Define **métodos genéricos** que pueden ser utilizados o sobrescritos.
- Ayuda a **reducir la duplicación de código**.

---

## 📚 Beneficios de usar superclases

| Beneficio                     | Descripción                                                      |
|------------------------------|------------------------------------------------------------------|
| Reutilización de código      | Métodos y atributos compartidos se escriben solo una vez.        |
| Organización jerárquica      | Permite modelar relaciones de generalización-especialización.    |
| Mantenibilidad del sistema   | Cambios en la superclase afectan a todas sus subclases.          |
| Polimorfismo y extensibilidad| Se pueden usar referencias a la superclase para acceder a objetos de subclases. |

---

## Ejemplo en Python

```python

class Vehiculo:
    def __init__(self, marca):
        self.marca = marca

    def encender(self):
        print(f"{self.marca} encendido.")


class Carro(Vehiculo):
    def encender(self):
        print(f"El carro {self.marca} está listo para arrancar.")

class Moto(Vehiculo):
    def encender(self):
        print(f"La moto {self.marca} está rugiendo.")
vehiculos = [Carro("Toyota"), Moto("Yamaha")]

for v in vehiculos:
    v.encender()