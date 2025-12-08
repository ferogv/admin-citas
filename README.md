# 🗓️ Sistema de administración de citas

* [Descripción del proyecto](https://github.com/DmonID/admin-citas#descripci%C3%B3n-del-proyecto)  
* [Instalación y configuración](https://github.com/DmonID/admin-citas#instalaci%C3%B3n-y-configuraci%C3%B3n)  
* [Uso del programa](https://github.com/DmonID/admin-citas#uso-del-programa)  
* [Créditos](https://github.com/DmonID/admin-citas#cr%C3%A9ditos)  
* [Licencia](https://github.com/DmonID/admin-citas#licencia)  

---

## 📌 Descripción del proyecto

**Sistema de administración de citas** es un programa en **Java** que simula la gestión de citas para un consultorio clínico.  
Permite dar de alta doctores, pacientes y citas, y relacionarlas entre sí.  
El sistema incluye control de acceso mediante administradores, quienes son los únicos con acceso completo.

### Funcionalidades principales
- **Alta de doctores:** registro con identificador, nombre, especialidad y contraseña.  
- **Alta de pacientes:** registro con identificador, nombre y contraseña.  
- **Creación de citas:** múltiples citas con identificador, fecha, hora y motivo, asociadas a un doctor y paciente.  
- **Control de acceso:** administradores pueden ver/modificar toda la información; doctores y pacientes solo la relacionada con ellos.  

---

## ⚙️ Instalación y configuración

1. Clonar el repositorio:
```bash
git clone https://github.com/DmonID/admin-citas.git
```

2. Navegar al directorio del proyecto:
```bash
cd admin-citas\src
```

3. Compilar los archivos fuente Java:
```bash
javac Doctor.java Paciente.java Cita.java Administrador.java SistemaCitas.java
```

4. Crear el archivo JAR ejecutable:
```bash
jar cfe SistemaCitas.jar SistemaCitas *.class
```
o, según versión de Java:
```bash
"C:\Program Files\Java\jdk-21\bin\jar" cfe SistemaCitas.jar SistemaCitas *.class
```

5. Ejecutar el programa:
```bash
java -jar SistemaCitas.jar
```

---

## 🚀 Uso del programa

1. Ingresar al sistema con identificador y contraseña de administrador, doctor o paciente.  
2. Seleccionar opción del menú principal: alta de doctores, alta de pacientes, crear cita o salir.  
3. Seguir las instrucciones mostradas en pantalla.  
4. Visualizar resultados en pantalla o en archivos de texto.  

---

## 👨‍💻 Créditos

Proyecto realizado por **@DmonID** como parte de la evidencia del curso *Computación en Java*.  

---

## 📄 Licencia

Este proyecto está bajo licencia **MIT**, lo que significa que puedes usar, copiar, modificar y distribuir el código libremente, siempre que reconozcas la autoría original y no lo uses con fines comerciales.  
