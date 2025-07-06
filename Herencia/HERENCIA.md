#  Herencia en Programación Orientada a Objetos (POO)

La **herencia** es uno de los pilares fundamentales de la Programación Orientada a Objetos (POO).  
Permite crear nuevas clases que **reutilizan atributos y métodos** de clases ya existentes.

---

## 🧠 ¿Qué es la herencia?

 **herede** 

- La clase hija **evita duplicación de código**.
- Permite crear **jerarquías de clases** de lo general a lo específico.
- Fomenta el principio de **reutilización** y **modularidad**.

---

##  Características principales

- ✅ Reutilización de código existente.
- ✅ La subclase **puede agregar** nuevos atributos o métodos.
- ✅ Puede **sobrescribir métodos heredados** (override).
- ✅ Facilita el mantenimiento y escalabilidad del código.

---

## 🎓 Ejemplo simple en Python

```python

class Animal:
    def __init__(self, nombre):
        self.nombre = nombre

    def hablar(self):
        print(f"{self.nombre} hace un sonido.")

class Perro(Animal):
    def hablar(self):
        print(f"{self.nombre} dice: ¡Guau!")
