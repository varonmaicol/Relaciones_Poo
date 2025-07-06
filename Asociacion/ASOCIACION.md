# 🤝 Asociación en Programación Orientada a Objetos (POO)

La **asociación** es un tipo de relación entre clases donde **dos o más objetos colaboran o interactúan entre sí**, pero **cada uno puede existir de manera independiente**.

---

## 🧠 Concepto Clave

 **conexión lógica**  **sin implicar pertenencia** 

- No hay propiedad ni control total entre los objetos.
- Los objetos involucrados **se relacionan temporalmente** para cumplir una funcionalidad.
- Es una relación común en sistemas orientados a objetos.

---

## 🎓 Ejemplo clásico: Profesor y Estudiante

```plaintext
Profesor enseña al Estudiante  
Estudiante aprende del Profesor  
→ Ambos existen de forma independiente

class Profesor:
    def __init__(self, nombre):
        self.nombre = nombre

    def ensenar(self):
        print(f"{self.nombre} está enseñando.")

class Estudiante:
    def __init__(self, nombre):
        self.nombre = nombre

    def aprender(self):
        print(f"{self.nombre} está aprendiendo.") 

prof = Profesor("Dr. García")
alumno = Estudiante("Ana")

prof.ensenar()
alumno.aprender()
