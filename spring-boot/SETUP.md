### Tips for becoming productive in developing Spring Boot backend APIs on Ubuntu

1. Install latest **Java version** using **APT** package manager
   ```
   sudo apt install default-jdk
   java -version
   ```

2. Install **IntelliJ IDEA** using snap package manager:
   ```
   sudo snap find "IntelliJ"
   sudo snap install intellij-idea
   ```
3. Generate Spring boot artifacts using [Spring Initializr](start.spring.io). Remember to fix dependencies to stable versions

4. Create empty repo on Github. Remember to toggle from `HTTPS` to `SSH`
   ```
   echo "# workhaven-hr" >> README.md
   git init
   git add README.md
   git commit -m "first commit"
   git branch -M main
   git remote add origin git@github.com:nathanbaleeta/workhaven-hr.git
   git push -u origin main
   ```
   
5. Maintain `IdeaProjects` home directory in the default location to avoid Maven builds from breaking
