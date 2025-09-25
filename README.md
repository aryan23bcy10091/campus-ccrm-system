# Campus Course & Records Manager (CCRM)

## Project Overview
Campus Course & Records Manager (CCRM) is a **console-based Java SE application** that enables an institute to manage students, courses, enrollments, and academic records. It provides grade computation, GPA calculation, transcript generation, and file utilities for import/export and backups.  

The project demonstrates core **Object-Oriented Programming (OOP)** principles, **Java SE APIs** (NIO.2, Streams, Date/Time API), as well as advanced concepts like **lambdas, recursion, and design patterns (Singleton & Builder)**.  

This project is built locally using **Java 17 (or higher)** and can be run via CLI.

***

## Features
- **Student Management**  
  - Add, update, list, deactivate students  
  - Enroll/un-enroll students to/from courses  
  - Print student profile & transcript  

- **Course Management**  
  - Add, update, list, deactivate courses  
  - Assign instructors  
  - Search/filter courses by **instructor**, **department**, **semester** (using Streams)  

- **Grades & GPA**  
  - Record marks & grades  
  - Compute GPA from grade points  
  - Transcript generation with polymorphism  

- **File Operations (NIO.2)**  
  - Import/export data in CSV format  
  - Backup data to a timestamped folder  
  - Recursive utilities for directory/file summaries  

- **CLI Workflow**  
  - Menu-driven interface using `switch`  
  - Loops (`for`, `while`, `do-while`, enhanced-for`) with jump controls (`break`, `continue`, labeled break`)  

***

## Technology Stack
- **Language:** Java SE (Java 17 recommended)  
- **IDE:** Eclipse (or IntelliJ)  
- **Libraries/APIs:** Java Streams, NIO.2, Date/Time API  
- **Design Patterns:** Singleton, Builder  
- **Version Control:** GitHub  

***

## Project Structure
```
edu.ccrm
├─ cli/        // Menu, input handling
├─ domain/     // Person, Student, Instructor, Course, Enrollment, enums
├─ service/    // Business logic: StudentService, CourseService, EnrollmentService
├─ io/         // File import/export, backup utilities
├─ util/       // Validators, comparators, recursive utilities
└─ config/     // Singleton, Builders
```

***

## Evolution of Java
- **1995:** Java 1.0 released by Sun Microsystems  
- **2004 (Java 5):** Generics, Enums, Annotations  
- **2011 (Java 7):** NIO.2, try-with-resources  
- **2014 (Java 8):** Lambdas, Streams, Date/Time API  
- **2017 (Java 9):** Modular system  
- **2021 (Java 17):** LTS release with sealed classes, pattern matching  

***

## Java Editions Comparison

| Edition | Use Case | Example |
|---------|----------|---------|
| **Java ME** | For embedded/mobile devices | Smart cards, set-top boxes |
| **Java SE** | Standard edition for desktop/server apps | Console apps & Swing apps |
| **Java EE** | Enterprise Edition with APIs for web & distributed apps | Servlet, JSP, EJB |

***

## Java Architecture
- **JVM (Java Virtual Machine):** Executes bytecode and provides platform independence.  
- **JRE (Java Runtime Environment):** Offers libraries + JVM to run Java applications.  
- **JDK (Java Development Kit):** Includes JRE + compiler + tools required for development.  

Process: **Source Code (.java) → Compiler → Bytecode (.class) → JVM Execution**

***

## Install & Setup (Windows)
1. Download [JDK 17+] from Oracle or OpenJDK.  
2. Install and set `JAVA_HOME` environment variable.  
3. Verify installation:  
   ```sh
   java -version
   ```
4. Install Eclipse IDE, create a new Java project, and import the source files.  

(Screenshots of installation & Eclipse setup are provided in the repo under `/screenshots`)  

***

## Usage
### Run the Program
1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/ccrm.git
   cd ccrm
   ```
2. Compile and run using CLI:
   ```sh
   javac -d bin src/edu/ccrm/Main.java
   java -cp bin edu.ccrm.Main
   ```

### Demo Flow
- Start program → AppConfig loads configuration  
- Menu appears with options:
  - Manage Students  
  - Manage Courses  
  - Enrollments & Grades  
  - Reports (e.g., GPA distribution)  
  - Import/Export Data  
  - Backup & Recursive File Summary  
  - Exit  

***

## Demonstrated Java Concepts
| Topic | File/Class |
|-------|-------------|
| Encapsulation | `Student.java` (private fields + getters/setters) |
| Inheritance | `Person.java` → `Student.java`, `Instructor.java` |
| Abstraction | `Person.java` (abstract methods) |
| Polymorphism | `TranscriptService.java` implementations |
| Singleton Pattern | `AppConfig.java` |
| Builder Pattern | `Course.Builder.java` |
| Enum | `Semester.java`, `Grade.java` |
| Exception Handling | `EnrollmentService.java`, `DuplicateEnrollmentException.java` |
| Recursion | `BackupService.java` (recursive folder size calc) |
| Streams & Lambdas | `CourseService.java` (search & filter) |
| Anonymous Class | Callback in CLI for exit handling |
| Nested Classes | `Course.java` (static nested class CourseCode) |

***

## Assertions
Assertions are used for validation (e.g., non-null IDs, credit bounds).  
Run program with assertions enabled:
```sh
java -ea -cp bin edu.ccrm.Main
```

***

 

***

## Acknowledgements
- Oracle Java Documentation  
- Effective Java by Joshua Bloch  
- Java SE 17 Cookbook resources  

***
