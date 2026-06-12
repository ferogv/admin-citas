# Appointment Management System

A CLI-based appointment scheduling system for clinical environments. Manages doctors, patients, and appointments through a role-based access model, with local binary persistence across sessions.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Language | Java (JDK 21) |
| Persistence | Java Object Serialization (`.dat`) |
| I/O | `java.util.Scanner` (stdin) |
| Build | Manual `javac` + `jar` |

No external dependencies.

---

## Features

- **Role-based access control** — only administrators can access the full system; credentials are validated on every session start
- **Doctor registration** — stores ID, name, specialty, username, and password
- **Patient registration** — stores ID, name, medical history, username, and password
- **Appointment creation** — links a doctor and patient with date and time; auto-incremented ID
- **Appointment listing** — displays all registered appointments for the current session
- **Session persistence** — data is serialized to `.dat` files on exit and reloaded on next launch

---

## Project Structure

```
admin-citas/
├── src/
│   ├── Administrador.java      # Admin entity with credentials
│   ├── Doctor.java             # Doctor entity (id, name, specialty, credentials)
│   ├── Paciente.java           # Patient entity (id, name, medical history, credentials)
│   ├── Cita.java               # Appointment entity linking Doctor and Patient
│   └── SistemaCitas.java       # Entry point — CLI menu, persistence logic, access control
├── db/
│   ├── doctores.csv            # Placeholder for future CSV-based persistence
│   ├── pacientes.csv           # Placeholder for future CSV-based persistence
│   └── citas.csv               # Placeholder for future CSV-based persistence
├── .gitignore
└── README.md
```

> Binary persistence files (`doctores.dat`, `pacientes.dat`, `citas.dat`) are generated at runtime in the project root.

---

## Setup

### Prerequisites

- JDK 21 or later

### Build & Run

```bash
# 1. Clone the repository
git clone https://github.com/ferogv/admin-citas.git
cd admin-citas/src

# 2. Compile
javac Administrador.java Doctor.java Paciente.java Cita.java SistemaCitas.java

# 3. Package
jar cfe SistemaCitas.jar SistemaCitas *.class
# On Windows with explicit JDK path:
# "C:\Program Files\Java\jdk-21\bin\jar" cfe SistemaCitas.jar SistemaCitas *.class

# 4. Run
java -jar SistemaCitas.jar
```

### Default Admin Credentials

```
Username: admin
Password: admin123
```

---

## Known Issues

- `SistemaCitas.java` line ~115 contains a typo (`System.out.prinln`) that causes a compilation error in the appointment listing method. A fix is planned as part of upcoming refactoring work.
- CSV files under `db/` are scaffolded but not yet integrated — persistence currently uses binary serialization only.

---

## Roadmap

- [ ] Fix compilation bug in `mostrarCitasRegistradas()`
- [ ] Migrate persistence layer from binary serialization to CSV / SQL
- [ ] Add doctor and patient login flows
- [ ] Input validation and error handling

---

## Author

**Fernando Gorostieta Vargas**
[linkedin.com/in/ferogv](https://linkedin.com/in/ferogv) · [github.com/ferogv](https://github.com/ferogv)
