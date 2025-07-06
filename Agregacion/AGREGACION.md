# 🧩 Agregación en Programación Orientada a Objetos (POO)

La **agregación** es un tipo de relación entre clases en la que una clase contiene a otra como parte de su estructura, pero **no es responsable total de su existencia**. Es decir, las instancias de la clase contenida pueden existir independientemente de la clase contenedora.

## 🧠 Concepto Clave

 **vínculo más débil** 

### ✅ Características principales:
- Relación de **todo-parte**, pero **sin dependencia fuerte**.
- Los objetos agregados **pueden vivir fuera** del objeto contenedor.
- Usada cuando los objetos contenidos **no deberían ser destruidos** junto al objeto principal.

---

## 🎓 Ejemplo: Salón de clases y Estudiantes

En este ejemplo, un **Salón de Clases** tiene varios **Estudiantes**, pero los estudiantes **pueden existir sin estar** en un salón.

```python
class Estudiante:
    def __init__(self, nombre):
        self.nombre = nombre

    def presentarse(self):
        print(f"Hola, soy {self.nombre}")

class SalonDeClases:
    def __init__(self, numero):
        self.numero = numero
        self.estudiantes = []

    def agregar_estudiante(self, estudiante):
        self.estudiantes.append(estudiante)

    def mostrar_estudiantes(self):
        for est in self.estudiantes:
            est.presentarse()
