## DAY-7 | NEXUS

Nexus Repository Manager: Nexus Repository Manager is a popular artifact repository management tool often used in DevOps environments. It serves as a central hub for storing and managing software artifacts such as binary files, libraries, and dependencies. The Nexus Repository Manager provides version control, access control, and distribution capabilities, making it easier for development and operations teams to collaborate on building and deploying software. By having a centralized repository, teams can ensure consistency, traceability, and efficient sharing of artifacts across the software development lifecycle.

## Real-world Scenario: Using Nexus Artifact Repository in a DevOps Environment

Imagine a software development team working on a web application that consists of multiple microservices. Each microservice has its own codebase, dependencies, and associated artifacts. In this scenario, the **Nexus Artifact Repository** can play a crucial role in managing these artifacts.

### **Centralized Artifact Storage**

The team can set up a Nexus Repository Manager as a central hub to store and manage the artifacts related to their microservices. This includes the application's binary files, libraries, frameworks, and other dependencies. Developers can publish their artifacts to the Nexus repository, ensuring a centralized location for easy access and distribution.

### **Dependency Management**

The Nexus Repository Manager allows the team to manage their dependencies effectively. Instead of relying on external repositories, which may have reliability or security concerns, the team can configure Nexus to proxy and cache external repositories such as Maven Central or npm. This ensures that the team has control over the versions of the dependencies being used and avoids potential issues caused by external repository downtime.

### **Continuous Integration and Deployment**

In a CI/CD pipeline, the Nexus repository serves as a source for storing build artifacts. When a developer commits code changes to the version control system, the CI server (e.g., Jenkins) can automatically build the code, run tests, and publish the resulting artifacts to the Nexus repository. Other downstream stages of the pipeline, such as deployment or testing environments, can then pull these artifacts from Nexus for further processes.

### **Artifact Versioning and Traceability**

Nexus provides version control capabilities, allowing the team to maintain different versions of their artifacts. This helps in tracking changes, rolling back to previous versions if necessary, and providing traceability throughout the software development lifecycle. It ensures that the team has a reliable history of the artifacts used in each release, aiding in troubleshooting and auditing purposes.

### **Collaboration and Access Control**

Nexus allows teams to set up access control policies, defining who can access and publish artifacts. This ensures that only authorized team members can deploy or modify artifacts in the repository. It promotes collaboration by providing a centralized platform for sharing artifacts among team members while maintaining control over access and permissions.

By leveraging the Nexus Artifact Repository in this scenario, the team can achieve better artifact management, dependency control, and collaboration. It helps to streamline the development and deployment processes, reduces the risk of using unreliable external repositories, and ensures consistency and traceability throughout the software development lifecycle.

### To install Nexus on Linux, follow these steps:

1. Prerequisites:
   - Ensure that Java Development Kit (JDK) is installed on your Linux system. Nexus requires Java to run. You can check if Java is installed by running the command `java -version` in the terminal. If Java is not installed, you can install it using the package manager of your Linux distribution.

2. Download Nexus:
   - Visit the Sonatype website and go to the Nexus download page: https://www.sonatype.com/nexus/repository-oss-download
   - Download the latest version of Nexus Repository Manager OSS (Open Source Edition). Look for the "Unix/Linux" distribution package in the list.
   - Alternatively, you can use the following command in the terminal to download Nexus:
     ```
     wget https://download.sonatype.com/nexus/3/latest-unix.tar.gz
     ```

3. Extract Nexus:
   - Open a terminal and navigate to the directory where the downloaded Nexus package is located.
   - Extract the package using the following command:
     ```
     tar -xf latest-unix.tar.gz
     ```

4. Configure Nexus:
   - Open the extracted Nexus directory.
   - In the `bin` folder, you will find a script called `nexus` (or `nexus.exe` for Windows). This is the Nexus startup script.
   - Make the script executable by running the following command:
     ```
     chmod +x nexus
     ```

5. Start Nexus:
   - Start Nexus by running the following command in the terminal:
     ```
     ./nexus start
     ```

6. Access Nexus Web UI:
   - Open a web browser and navigate to `http://localhost:8081`. This is the default URL for accessing Nexus.
   - The first time you access Nexus, you will be prompted to set up the administrator credentials. Follow the on-screen instructions to create an admin user.

That's it! Nexus is now installed and running on your Linux system. You can proceed to configure Nexus, create repositories, and manage artifacts using the Nexus Web UI.

## Install Nexus using Docker

```
docker run -d --name nexus -p 8081:8081 sonatype/nexus3
```