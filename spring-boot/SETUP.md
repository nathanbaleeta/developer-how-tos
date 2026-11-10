### Tips for becoming productive in developing Spring Boot backend APIs on Ubuntu

1. Install latest **Java version** using **APT** package manager
   ```
   sudo apt install default-jdk
   ```

2. Install **IntelliJ IDEA** using snap package manager:
   ```
   sudo snap find "IntelliJ"
   sudo snap install intellij-idea
   java -version
   ```
3. Generate Spring boot artifacts using [Spring Initializr](start.spring.io). Remember to fix dependencies to stable versions
   
4. Maintain `IdeaProjects` home directory in the default location to avoid Maven builds from breaking
