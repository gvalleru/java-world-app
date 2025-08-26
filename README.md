# 🌍 Java World App

A minimal Spring Boot web application built with Maven and Java 17+, packaged as a `.war`, and deployable to Apache Tomcat.

---

## ✅ Features

- Java 17+ (tested with Java 23)
- Spring Boot 3.2.2
- WAR packaging
- Maven 3.9.x build system
- Single REST endpoint: `/hello`

---

## 🔧 Prerequisites

Make sure the following are installed:

```bash
java --version
# java 17 or later (tested with Java 23)

mvn -v
# Apache Maven 3.9.11 or later
```

## 🚀 Getting Started

```bash
git clone git@github.com:gvalleru/java-world-app.git
cd java-world-app
git checkout main
git pull
```

## 🛠 Build the App

```bash
mvn clean package
```

Expected part of output:

```bash
[INFO] Building java-world-app 0.0.1-SNAPSHOT
[INFO] Packaging webapp
[INFO] Building war: .../target/java-world-app.war
[INFO] BUILD SUCCESS
```

The generated WAR file will be in: `target/java-world-app.war`

## 🧩 Deploy to Tomcat

```bash
# Copy WAR to Tomcat’s webapps directory:

cp target/java-world-app.war ~/Documents/tools/apache-tomcat-10.1.44/webapps/

# Start Tomcat:

cd ~/Documents/tools/apache-tomcat-10.1.44/bin
./startup.sh

# Monitor logs:

tail -f ../logs/catalina.out

# Expected logs:

Deploying web application archive [java-world-app.war]
:: Spring Boot :: (v3.2.2)
Started JavaWorldAppApplication...
```

## 🌐 Test the Endpoint

Open in browser or run:

```bash
curl http://localhost:8080/java-world-app/hello
```

Expected response: `Hello, world from Java World App!`
