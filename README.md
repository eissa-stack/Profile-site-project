# VProfile Project: Java Web Application with CI/CD Pipeline

A complete Java web application with a fully configured CI/CD pipeline using Jenkins, SonarQube, Nexus, and other DevOps tools.

## Project Overview

This project demonstrates a robust CI/CD implementation for a Java-based web application that uses Spring MVC architecture. The application has been configured with a comprehensive Jenkins pipeline that handles the entire software delivery process from build to deployment.

## Technologies Used

### Application Stack
- Java 8/11
- Spring MVC
- Spring Security
- Spring Data JPA
- Maven
- JSP
- MySQL 8
- Memcached
- RabbitMQ
- ElasticSearch

### DevOps Tools
- Jenkins (CI/CD Pipeline)
- SonarQube (Code Quality Analysis)
- Nexus Repository (Artifact Management)
- Docker (Containerization)
- Git (Version Control)

## Pipeline Features

The Jenkins pipeline in this project includes the following stages:

1. **BUILD**: Compiles the application and creates the WAR file
2. **UNIT TEST**: Runs unit tests to verify individual components
3. **INTEGRATION TEST**: Executes integration tests to verify component interactions
4. **CODE ANALYSIS WITH CHECKSTYLE**: Verifies code adheres to coding standards
5. **CODE ANALYSIS WITH SONARQUBE**: Performs in-depth code quality analysis
6. **PUBLISH TO NEXUS**: Uploads build artifacts to Nexus Repository Manager

## Prerequisites

To run this project locally, you need:

- JDK 11
- Maven 3
- MySQL 8
- Jenkins
- SonarQube
- Nexus Repository Manager

## Setup Instructions

### Database Setup

1. Install MySQL 8
2. Import the database dump file:
   ```
   mysql -u <user_name> -p accounts < src/main/resources/db_backup.sql
   ```

### Application Setup

1. Clone this repository
2. Configure the application properties according to your environment
3. Build the application:
   ```
   mvn clean install
   ```

### Jenkins Pipeline Setup

1. Install Jenkins and required plugins:
   - Maven Integration
   - Pipeline
   - SonarQube Scanner
   - Nexus Artifact Uploader

2. Configure Jenkins credentials for:
   - SonarQube
   - Nexus Repository

3. Create a new Pipeline job using the provided Jenkinsfile

## Environment Variables

The Jenkins pipeline uses the following environment variables:

- `NEXUS_VERSION`: Version of Nexus (set to "nexus3")
- `NEXUS_PROTOCOL`: Protocol for Nexus URL (set to "http")
- `NEXUS_URL`: URL of Nexus server
- `NEXUS_REPOSITORY`: Name of the repository in Nexus
- `NEXUS_CREDENTIAL_ID`: Jenkins credential ID for Nexus authentication

## Project Structure

```
├── Jenkinsfile               # Jenkins pipeline configuration
├── pom.xml                   # Maven dependencies and build configuration
├── src/                      # Source code
│   ├── main/                 # Application code
│   │   ├── java/             # Java code
│   │   ├── resources/        # Configuration files
│   │   └── webapp/           # Web resources
│   └── test/                 # Test code
```

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin feature-name`
5. Submit a pull request

## Future Improvements

- Add Docker containerization
- Implement Kubernetes deployment
- Add automated testing for frontend components
- Configure blue/green deployment strategy

## License

[Include your license information here]

## Acknowledgements

- Spring Framework
- Jenkins
- SonarQube
- Nexus Repository Manager

---

This project showcases my DevOps skills, particularly in implementing CI/CD pipelines with Jenkins and integrating various tools like SonarQube and Nexus Repository Manager.
