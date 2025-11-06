# Jenkins Free Project

## Project Overview

This is a simple Jenkins CI/CD project that demonstrates the setup of a basic Jenkins pipeline for a Python application. The project showcases how to integrate Jenkins with a Python script and implement automated build and test stages.

## Project Structure

The project contains the following files:

### 1. `mypythonapp.py`
A simple Python application that prints a message to the console.

**What it does:**
- Prints: "Hello i am a devops engineer and i am creating a pipepline for my python app"
- Serves as a basic Python application for demonstrating the Jenkins pipeline

**Usage:**
```bash
python3 mypythonapp.py
```

### 2. `Jenkinsfile`
A Jenkins declarative pipeline configuration file that defines the CI/CD pipeline for the Python application.

**Pipeline Stages:**

#### Build Stage
- **Purpose:** Executes the Python application
- **Actions:**
  - Logs "Building.." message
  - Runs `python3 mypythonapp.py` to execute the application

#### Test Stage
- **Purpose:** Validates that the application output contains expected content
- **Actions:**
  - Logs "Testing.." message
  - Runs the Python application and checks if output contains "devops" using grep
  - Pipeline fails if "devops" is not found in the output

## What Has Been Done

1. **Created a Python Application**: A simple Python script that outputs a DevOps-related message
2. **Implemented Jenkins Pipeline**: Set up a declarative Jenkins pipeline with two stages (Build and Test)
3. **Automated Testing**: Implemented a basic test that validates the application output
4. **Version Control**: Project is tracked using Git with proper commit history

## Jenkins Pipeline Flow

```
Start
  ↓
Build Stage
  ↓ (Execute Python app)
  ↓
Test Stage
  ↓ (Verify output contains "devops")
  ↓
Success/Failure
```

## Prerequisites

To run this project, you need:
- Python 3.x installed
- Jenkins server configured
- Access to the repository in Jenkins

## How to Use

### Running Locally

1. Clone the repository:
```bash
git clone https://github.com/IsthatAyus/jenkins_freeproject.git
cd jenkins_freeproject
```

2. Run the Python application:
```bash
python3 mypythonapp.py
```

### Running with Jenkins

1. Create a new Jenkins Pipeline job
2. Configure the job to use this repository
3. Point Jenkins to the `Jenkinsfile` in the repository root
4. Run the pipeline

The pipeline will automatically:
- Execute the Python application in the Build stage
- Test the output in the Test stage
- Report success or failure

## Pipeline Configuration

The pipeline uses:
- **Agent:** `any` - Can run on any available Jenkins agent
- **Stages:** Two stages (Build and Test)
- **Shell Commands:** Uses `sh` step to execute shell commands
- **Validation:** Uses `grep` to validate application output

## Learning Objectives

This project demonstrates:
- Basic Jenkins pipeline syntax (declarative)
- Integration of Python applications with Jenkins
- Simple automated testing using shell commands
- CI/CD pipeline stages (Build and Test)
- Version control practices

## Future Enhancements

Potential improvements could include:
- Adding more comprehensive tests
- Implementing deployment stage
- Adding code quality checks (linting)
- Integrating with other DevOps tools
- Adding notifications (email, Slack, etc.)

## Author

Created as a learning project for Jenkins CI/CD pipeline implementation with Python applications.
