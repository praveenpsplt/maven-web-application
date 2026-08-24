# Maven Web Application CI/CD Project

## Project Overview

This project is a Java Maven web application packaged as a WAR file. The Maven project uses Java 8 and Spring Framework dependencies. The project is suitable for practicing a DevOps CI/CD workflow with Git, GitHub, Maven, Jenkins, SonarQube, Nexus, and application deployment.

## Technologies Used

- Java 8
- Maven
- Spring Framework 5.1.2
- Git
- GitHub
- Jenkins
- SonarQube
- Nexus Repository
- Apache Tomcat
- Linux

## Project Details

| Property | Value |
|---|---|
| Group ID | `com.mt` |
| Artifact ID | `maven-web-application` |
| Packaging | `war` |
| Version | `0.0.1-SNAPSHOT` |
| Java Version | `1.8` |
| Final Build Name | `maven-web-application` |

The project configuration confirms WAR packaging, Java 8, and the Maven final artifact name. 

## CI/CD Workflow

```text
Developer
    |
    v
   Git
    |
    v
  GitHub
    |
    v
 Jenkins Pipeline
    |
    +----> Maven Build & Test
    |
    +----> SonarQube Code Analysis
    |
    +----> Nexus Repository
    |
    v
 Apache Tomcat
    |
    v
Application
```

## Maven Build

Build the application with:

```bash
mvn clean package
```

The Maven project is configured to produce a WAR package named:

```text
maven-web-application.war
```

## Run the Application

The project contains Jetty Maven plugin configuration with the application context path:

```text
/maven-web-application
```

The configured Jetty scan interval is 10 seconds.

## Jenkins

A Jenkins pipeline can automate:

1. Source code checkout
2. Maven build
3. Testing
4. SonarQube analysis
5. Artifact handling
6. Deployment

The repository contains Jenkins pipeline files for this automation.

## Nexus Repository

The Maven configuration contains release and snapshot repository settings under `distributionManagement`.

> Before using the project in a real environment, configure repository credentials securely in Jenkins/Maven settings rather than storing credentials in source code.

## Project Structure

```text
.
├── .gitignore
├── Jenkinsfile
├── JenkinsfileDeclarative
├── docker-compose.yml
├── pom.xml
└── README.md
```

## Git Commands

```bash
git clone <repository-url>
cd maven-web-application

git status
git add .
git commit -m "Update project"
git push origin main
```

## Useful Maven Commands

```bash
mvn clean
mvn test
mvn package
mvn clean package
```

## DevOps Learning Objectives

This project can be used to practice:

- Git branching and GitHub workflow
- Maven build and packaging
- Jenkins CI/CD pipelines
- Static code analysis with SonarQube
- Artifact management with Nexus
- WAR deployment to Tomcat
- Linux-based deployment and troubleshooting

## Author

Praveen
