# Java Event-Driven Programming

A practical Java learning repository featuring hands-on exercises, implementation guides, and projects focused on Event-Driven Programming, the Observer Design Pattern, Swing GUI development, JavaFX, and a final University Management System capstone project.

---

## Table of Contents

- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Launching Applications](#launching-applications)
- [Course Roadmap](#course-roadmap)
- [Script Options](#script-options)
- [Final Project: University Management System](#final-project-university-management-system)
- [Executing Individual Java Files](#executing-individual-java-files)
- [Author Information](#author-information)

---

## Prerequisites

Before running the projects, ensure the following tools are installed:

| Software | Requirement |
|---|---|
| Java Development Kit | JDK 11 or later (JDK 17 or 21 recommended) |
| Apache Maven | Required for JavaFX projects in Weeks 6–10 |

To confirm that your development environment is configured correctly, execute:

```bash
java -version
javac -version
mvn -version
```

---

## Getting Started

### Step 1: Compile the Repository

The repository includes build scripts that compile Java source files across the different project directories.

| Environment | Standard Build | Clean Build |
|---|---|---|
| Git Bash / macOS / Linux | `./build` | `./build --clean` |
| Windows CMD / PowerShell | `.\build.bat` | `.\build.bat --clean` |
| npm (Optional) | `npm run build` | `npm run build:clean` |

### Step 2: Access the Interactive Launcher

Use the interactive menu to navigate and execute activities from different course modules.

**For Git Bash, macOS, and Linux:**

```bash
./scripts/run-all.sh
```

**For Windows PowerShell:**

```powershell
.\scripts\run-all.ps1
```

> **Windows Git Bash users:** Use forward slashes when executing scripts, such as `./scripts/run-all.sh`. Avoid Windows-style backslashes.

---

## Launching Applications

### Direct GUI Launchers (Weeks 2–5)

Individual graphical launchers can be started directly from the repository root using the following commands:

```bash
# Week 2 - Observer Pattern
java -cp Week02-observer-pattern Week2Launcher

# Week 3 - Swing GUI
java -cp week03-swing-gui Week3Launcher

# Week 4 - Swing Event Handling
java -cp week04-event-handling Week4Launcher

# Week 5 - Advanced Swing
java -cp week05-advanced-swing Week5Launcher
```

### JavaFX Applications (Weeks 6–10)

JavaFX applications are managed through Maven. Run each project using its corresponding `pom.xml` file:

```bash
# Week 6 - Modern JavaFX
mvn -f week06-javafx/pom.xml javafx:run

# Week 7 - JavaFX Event Handling
mvn -f week07-javafx-events/pom.xml javafx:run

# Week 8 - JavaFX Properties and Bindings
mvn -f week08-javafx-bindings/pom.xml javafx:run

# Week 9 - Asynchronous JavaFX
mvn -f week09-async-javafx/pom.xml javafx:run

# Week 10 - University Management System
mvn -f UniversitySystem/pom.xml javafx:run
```

---

## Course Roadmap

The repository is organized into ten weekly modules, progressing from foundational event-driven concepts to advanced GUI development and a complete desktop application.

| Week | Learning Area | Source Code | Learning Material | Execution Script |
|---|---|---|---|---|
| **01** | Event-Driven Fundamentals and Bug Fixes | [Week1_Activity](Week1_Activity/) | [Week 1 Guide](documentation/Week%201%20Self%20paced%20Activity.md) | `./scripts/run-week1.sh` / `.\scripts\run-week1.ps1` |
| **02** | Observer Design Pattern | [Week02-observer-pattern](Week02-observer-pattern/) | [Week 2 Guide](documentation/Week%202%20Self%20paced%20Activity.md) | `./scripts/run-week2.sh` / `.\scripts\run-week2.ps1` |
| **03** | Swing GUI and Layout Management | [week03-swing-gui](week03-swing-gui/) | [Week 3 Guide](documentation/Week%203%20Self%20paced%20Activity.md) | `./scripts/run-week3.sh` / `.\scripts\run-week3.ps1` |
| **04** | Event Handling with Swing | [week04-event-handling](week04-event-handling/) | [Week 4 Guide](documentation/Week%204%20Self%20paced%20Activity.md) | `./scripts/run-week4.sh` / `.\scripts\run-week4.ps1` |
| **05** | Advanced Swing Components: JTable, Menus and Dialogs | [week05-advanced-swing](week05-advanced-swing/) | [Week 5 Guide](documentation/Week%205%20Advanced%20Swing%20Components.md) | `./scripts/run-week5.sh` / `.\scripts\run-week5.ps1` |
| **06** | Introduction to Modern JavaFX | [week06-javafx](week06-javafx/) | [Week 6 Guide](documentation/Week%206%20Self%20Paced%20Guide_Introduction%20to%20Modern%20JavaFX.md) | `./scripts/run-week6.sh` / `.\scripts\run-week6.ps1` |
| **07** | Event Handling in JavaFX | [week07-javafx-events](week07-javafx-events/) | [Week 7 Guide](documentation/Week%207%20Self%20Paced%20Guide_Event%20Handling%20in%20JavaFX.md) | `./scripts/run-week7.sh` / `.\scripts\run-week7.ps1` |
| **08** | JavaFX Properties and Bindings | [week08-javafx-bindings](week08-javafx-bindings/) | [Week 8 Guide](documentation/Week%208%20Self-Paced%20Guide_%20Properties%20and%20Bindings%20in%20JavaFX.md) | `./scripts/run-week8.sh` / `.\scripts\run-week8.ps1` |
| **09** | Asynchronous Programming in JavaFX | [week09-async-javafx](week09-async-javafx/) | [Week 9 Guide](documentation/Week%209%20Self%20Paced%20Guide_Asynchronous%20Programming%20in%20JavaFX.md) | `./scripts/run-week9.sh` / `.\scripts\run-week9.ps1` |
| **10** | Capstone: University Management System | [UniversitySystem](UniversitySystem/) | [Week 10 Guide](documentation/Week%2010%20Final%20Project%20Capstone%20-%20University%20Management%20System.md) | `./scripts/run-university.sh` / `.\scripts\run-university.ps1` |

---

## Script Options

The weekly execution scripts provide additional options for controlling how activities are launched.

| Option | Description |
|---|---|
| `--all` / `-All` | Executes all activities available for the selected week. |
| `--launcher` / `-Launcher` | Opens the graphical launcher for Weeks 2–9. |

---

## Final Project: University Management System

The tenth module introduces a JavaFX desktop application integrated with **Neon Serverless PostgreSQL**.

The application uses a cloud-hosted PostgreSQL database rather than a locally installed MySQL server. This approach was chosen to explore Neon and make the application easier to run without requiring users to install and configure a local database.

### Database Configuration

Follow these steps to configure the application:

**1. Create a Neon Database**

Visit [Neon](https://neon.tech), create a free database, and obtain its PostgreSQL connection string.

**2. Configure Environment Variables**

Copy the repository's `.env.example` file into the root directory and rename the copy to `.env` or `.env.local`.

**3. Set the Database Connection**

Add your Neon connection string to the `DATABASE_URL` environment variable:

```env
DATABASE_URL="postgresql://USER:PASSWORD@YOUR-NEON-HOST.neon.tech/neondb?sslmode=require"
```

> **Automatic Database Initialization:** The `programs` and `students` tables, together with sample program records, are generated automatically when the application runs for the first time.

### Starting the Application

To launch the University Management System through Maven:

```bash
mvn -f UniversitySystem/pom.xml javafx:run
```

Alternatively, use npm:

```bash
npm run start:university
```

### Database Integration Testing

Run the following command to execute the university database integration tests:

```bash
npm run test:university
```

---

## Executing Individual Java Files

For Weeks 1–5, individual Java activities can also be compiled and executed manually without using the interactive launcher.

**General command structure:**

```bash
javac <folder>/<FileName>.java
java -cp <folder> <MainClassName>
```

**Example: Running the Event-Driven Calculator**

```bash
# Compile the Java source file
javac Week1_Activity/EventDrivenCalculator.java

# Execute the compiled application
java -cp Week1_Activity EventDrivenCalculator
```

---

## Author Information

**Author:** Laban Githinji

**Email:** [githinjilaban445@gmail.com](mailto:githinjilaban445@gmail.com)

---

*This repository documents practical learning and implementation of Java Event-Driven Programming concepts, progressing from basic event handling to modern JavaFX development and database-integrated desktop applications.*