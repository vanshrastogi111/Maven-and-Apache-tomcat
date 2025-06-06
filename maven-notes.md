# 📦 Apache Maven – DevOps Build Automation

This project demonstrates how to use **Apache Maven** for automating the build lifecycle, managing dependencies, and packaging Java applications in a DevOps workflow.

Maven is an essential tool for Java developers and DevOps engineers, enabling consistent builds, repeatable deployments, and seamless integration into CI/CD pipelines.

---

## 🚀 What This Project Covers

- Creating a Maven project using `pom.xml`
- Managing external libraries and dependencies
- Compiling, testing, and packaging Java applications
- Understanding Maven lifecycles (clean, default, site)
- Running common Maven commands in a CI/CD-ready style

---

## 🧠 Why Use Maven?

- Automates build steps like compile, test, package
- Manages dependencies via Maven Central and `pom.xml`
- Works with CI tools like Jenkins, GitHub Actions, GitLab CI
- Supports WAR/JAR packaging for deployment
- Enables code quality tools via plugins (JUnit, JaCoCo, SpotBugs)

---

## 🏗️ Maven Project Structure

my-java-app/
├── pom.xml
└── src/
├── main/
│ ├── java/
│ └── resources/
└── test/
└── java/

php-template
Copy
Edit

---

## 🔁 Maven Build Lifecycles

### 🔹 Clean Lifecycle
| Phase  | Description                         |
|--------|-------------------------------------|
| clean  | Deletes previous build artifacts    |

### 🔹 Default Lifecycle
| Phase     | Description                            |
|-----------|----------------------------------------|
| validate  | Checks the project structure            |
| compile   | Compiles Java source code               |
| test      | Runs unit tests                         |
| package   | Packages app into `.jar` or `.war`      |
| install   | Installs build artifact into `.m2` repo |
| deploy    | Pushes artifact to remote repo (Nexus)  |

### 🔹 Site Lifecycle
| Phase         | Description                         |
|---------------|-------------------------------------|
| site          | Generates project documentation     |
| site-deploy   | Publishes docs to web server        |

---
### Maven Command Examples:

Here are some common Maven commands:

- `mvn compile`: Compiles the project's source code.
- `mvn test`: Runs unit tests against compiled code.
- `mvn package`: Packages the compiled code into a distributable format.
- `mvn install`: Installs the package into the local repository.
- `mvn deploy`: Deploys the package to a remote repository.
- `mvn site`: Generates project documentation and reports.
- `mvn site-deploy`: Deploys the generated documentation to a remote web server.  
- `mvn clean`: Executes the clean phase, deleting any previous build outputs. 

---
## ⚙️ Sample `pom.xml`

```xml
<project xmlns="http://maven.apache.org/POM/4.0.0" ...>
  <modelVersion>4.0.0</modelVersion>
  <groupId>com.example</groupId>
  <artifactId>demo-app</artifactId>
  <version>1.0-SNAPSHOT</version>
  <packaging>jar</packaging>

  <dependencies>
    <dependency>
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>4.13.2</version>
      <scope>test</scope>
    </dependency>
  </dependencies>

  <build>
    <plugins>
      <plugin>
        <artifactId>maven-compiler-plugin</artifactId>
        <version>3.8.1</version>
        <configuration>
          <source>1.8</source>
          <target>1.8</target>
        </configuration>
      </plugin>
    </plugins>
  </build>
</project>

