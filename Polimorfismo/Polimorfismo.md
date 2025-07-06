# Polimorfismo en Programación Orientada a Objetos (POO)

El **polimorfismo** es un principio fundamental de la Programación Orientada a Objetos (POO) que permite que **distintas clases implementen un mismo método de formas diferentes**.

---

##  ¿Qué significa "polimorfismo"?

> Proviene del griego *"poli"* (muchos) y *"morphos"* (formas)
 **un mismo método puede tener distintos comportamientos** 

---

##  ¿Para qué sirve?

- Permite escribir **código más flexible y reutilizable**.
- Facilita el **mantenimiento y extensión** del software.
- Se basa en la **interfaz común** que diferentes clases pueden compartir.

---

## Ejemplo práctico en Python

```python
class Animal:
    def hablar(self):
        print("El animal hace un sonido.")

class Perro(Animal):
    def hablar(self):
        print("El perro dice: ¡Guau!")

class Gato(Animal):
    def hablar(self):
        print("El gato dice: ¡Miau!")
        
animales = [Perro(), Gato(), Animal()]

for animal in animales:
    animal.hablar()