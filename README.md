# GraalVM-demo

## Build for Windows:

1. Download Visual Studio Tools 2022
2. Download GraalVM JDK + switch JDK
3. Build native image: ```./mvnw -Pnative native:compile```

Reference: [Installation on Windows Platforms](https://www.graalvm.org/latest/docs/getting-started/windows/)

## Build for Linux (WSL2)

Set-up WSL2:
1. Open cmd (admin), install Ubuntu: ```wsl --install -d Ubuntu```
2. (Optional) Switch WSL version: ```wsl --set-version Ubuntu 2```
3. Download dependencies required for building native executable: ```apt install gcc g++ binutils zlib1g-dev```
4. Check Java works: ```java --version```

Install Java on WSL2 Ubuntu:
1. Download Java: ```wget https://download.oracle.com/graalvm/21/latest/graalvm-jdk-21_linux-x64_bin.tar.gz```
2. Unzip:  ```tar -xzf graalvm-jdk-....tar.gz```
3. Set JAVA_HOME: ```export JAVA_HOME=/path/to/<graalvm>```
4. Update PATH: ```export PATH=/path/to/<graalvm>/bin:$PATH```

Build native Linux executable: ```./mvnw -Pnative native:compile```

Reference: [Installation on Linux Platforms](https://www.graalvm.org/latest/docs/getting-started/linux/)