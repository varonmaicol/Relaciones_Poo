# ⚙️ Composición en Programación Orientada a Objetos (POO)

La **composición** es una relación fuerte entre clases. En esta relación, **una clase contiene a otra**, y **la clase contenida no puede existir independientemente** de la clase principal.

---

## 🧠 Concepto Clave

 **depende completamente** 

- Relación "todo-parte" con **dependencia total**.
- El objeto contenido se **crea y destruye** junto al objeto principal.
- No puede compartirse con otras instancias.

---

## 🚗 Ejemplo: Carro y Motor

```python
class Motor:
    def __init__(self, tipo):
        self.tipo = tipo

    def encender(self):
        print(f"Motor {self.tipo} encendido.")

class Carro:
    def __init__(self, marca, tipo_motor):
        self.marca = marca
        self.motor = Motor(tipo_motor)  

    def arrancar(self):
        print(f"Arrancando {self.marca}")
        self.motor.encender()
