# Clínica Veterinaria

Sistema de gestión para una clínica veterinaria, desarrollado en Java como proyecto del primer parcial de Programación Orientada a Objetos. Funciona por consola mediante un menú de opciones.

## Descripción

El programa permite administrar el funcionamiento básico de una clínica veterinaria:

- Registrar clientes (dueños de mascotas) y veterinarios.
- Registrar mascotas asociadas a un cliente.
- Agendar citas entre una mascota y un veterinario, evitando que un veterinario tenga dos citas activas a la misma fecha y hora.
- Confirmar o cancelar citas.
- Registrar la consulta de una cita (diagnóstico, tratamiento, costo y observaciones).
- Listar clientes con sus mascotas, veterinarios y citas.
- Consultar el historial médico de una mascota.

Los datos se guardan en memoria mientras el programa está en ejecución.

## Conceptos de POO aplicados

- **Clase abstracta:** `Persona`.
- **Herencia:** `Cliente` y `Veterinario` extienden de `Persona`.
- **Interfaz:** `IGestionable`, implementada por las clases del modelo.
- **Polimorfismo:** el método `mostrarInformacion()` se invoca desde `Main` sobre cualquier objeto `IGestionable`.
- **Encapsulamiento:** atributos privados con getters.
- **Colecciones:** uso de `ArrayList`.

## Estructura del proyecto

```
ClinicaVeterinaria/
└── src/clinicaveterinaria/
    ├── Main.java                      # Menú y entrada por consola
    ├── GestorClinicaVeterinaria.java  # Lógica de registro y búsqueda
    ├── Persona.java                   # Clase abstracta
    ├── Cliente.java
    ├── Veterinario.java
    ├── Mascota.java
    ├── Cita.java
    ├── Consulta.java
    └── IGestionable.java              # Interfaz
```

## Tecnologías utilizadas

- Java (JDK)
- NetBeans IDE (proyecto Ant)
- Git y GitHub para el control de versiones

## Instrucciones de ejecución

### Con NetBeans

1. Clona o descarga este repositorio.
2. En NetBeans, ve a **File → Open Project** y selecciona la carpeta `ClinicaVeterinaria`.
3. Haz clic derecho sobre el proyecto y elige **Run** (o presiona `F6`).
4. Usa el menú que aparece en la consola de salida.

El proyecto está configurado con nivel de Java 26 en NetBeans. Si tu JDK es más antiguo, ve a **Properties → Sources** y baja el valor de **Source/Binary Format** a la versión que tengas instalada.

### Desde la terminal

Con el JDK instalado, desde la carpeta `ClinicaVeterinaria`:

```bash
mkdir out
javac -encoding UTF-8 -d out src/clinicaveterinaria/*.java
java -cp out clinicaveterinaria.Main
```

## Uso básico

Para agendar una cita, registra los datos en este orden:

1. Opción **1**: registrar cliente.
2. Opción **2**: registrar veterinario (se identifica por su **código de licencia**).
3. Opción **3**: registrar mascota (con la cédula del cliente).
4. Opción **4**: agendar cita (cédula del cliente, ID de la mascota y código de licencia del veterinario).

## Autor

Nombre del estudiante: _completar_
Materia: Programación Orientada a Objetos
