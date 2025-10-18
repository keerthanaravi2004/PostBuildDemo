PostBuildDemo - Jenkins Maven Integration Project
📘 Project Overview

This project demonstrates the integration of Maven and Jenkins for automating the build, test, and deployment pipeline of a simple Java application.
It covers the complete CI/CD lifecycle — including GitHub repository linkage, automated testing, artifact generation, and post-build actions like email notifications and artifact archiving.

🚀 Key Objectives

Automate the build process using Apache Maven

Integrate GitHub for source control

Configure Jenkins to automatically trigger builds

Execute unit tests and publish results

Package the project into a JAR artifact

Implement post-build actions such as:

Archiving build artifacts

Sending build status via Email Notifications

Conditional build steps for success/failure handling

🧱 Technologies & Tools Used
Tool	Purpose
Apache Maven 3.9.11	Build automation and dependency management
Jenkins	Continuous Integration tool
GitHub	Source code version control
Java 8 / JDK	Programming language for building the app
JUnit	Unit testing framework
Email Extension Plugin	For post-build notifications
WS Cleanup Plugin	Cleans workspace before every build
⚙ Project Structure
PostBuildDemo/
│
├── src/
│   ├── main/java/com/devops/postbuild/App.java
│   └── test/java/com/devops/postbuild/AppTest.java
│
├── pom.xml
└── README.md

🧩 Jenkins Pipeline Configuration

Pipeline Type: Freestyle Project (PostBuildDemoPipeline)

Steps Configured:

Source Code Management (SCM):

Repository URL: https://github.com/keerthanaravi2004/PostBuildDemo.git

Branch: main

Build Trigger:

Manually or via GitHub webhook (optional)

Build Step:

mvn clean install


Post-Build Actions:

Archive Artifacts:

target/*.jar


Publish JUnit Test Results:

*/target/surefire-reports/.xml


Email Notification:
Sends an automated mail when build succeeds/fails.

🧪 Build Output Summary
Stage	Result
Clean Workspace	✅ Successful
Clone Repository	✅ Successful
Compile Source Code	✅ Successful
Run Unit Tests	✅ All tests passed
Package JAR File	✅ Generated PostBuildDemo-1.0-SNAPSHOT.jar
Archive Artifact	✅ Stored successfully
Email Notification	✅ Triggered successfully
Final Build Status	🎯 BUILD SUCCESS
📦 Artifact Location

After a successful build, the artifact is generated and stored at:

target/PostBuildDemo-1.0-SNAPSHOT.jar


In Jenkins:

C:\ProgramData\Jenkins\.jenkins\workspace\PostBuildDemoPipeline\target\PostBuildDemo-1.0-SNAPSHOT.jar

📬 Email Notification Setup

Go to Jenkins → Manage Jenkins → Configure System

Under E-mail Notification:

SMTP Server: smtp.gmail.com

User Name: <your Gmail ID>

Password: App Password (generated from Google Account)

Port: 465 (SSL) or 587 (TLS)

Test configuration by sending a test mail.

📈 Future Enhancements

Add integration tests using Failsafe plugin.

Implement a downstream job trigger on build success.

Configure GitHub Webhooks for automatic builds.

Include Docker packaging and deployment pipeline.

🧠 Learning Outcomes

Understood Maven build lifecycle: clean → compile → test → package → install

Configured Jenkins for end-to-end CI/CD automation

Learned post-build integrations like artifact archiving and notifications

Experienced version control and automated testing in real CI workflows

👩‍💻 Developed By

Keerthana Ravi
Jenkins & Maven CI/CD Project | 2025
