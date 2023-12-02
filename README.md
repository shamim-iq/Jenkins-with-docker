# Sample Jenkins Pipeline

This repository contains a simple Jenkins Pipeline written in Groovy. The pipeline is designed to run a basic test inside a Docker container with Node.js 16.

## Usage

1. Make sure you have Jenkins installed and configured.
2. Copy the content of the Jenkinsfile in this repository.

    ```groovy
    pipeline {
        agent {
            docker { image 'node:16-alpine' }
        }
        stages {
            stage('Test') {
                steps {
                    sh 'node --version'
                    sh 'echo "Task successful.....!!"'
                }
            }
        }
    }
    ```

3. Create a new pipeline in Jenkins.
4. Paste the Jenkinsfile content into the pipeline script section.
5. Run the pipeline.

## What the Pipeline Does

1. **Agent Configuration:**
   - The pipeline runs inside a Docker container based on the 'node:16-alpine' image.

2. **Stages:**
   - The pipeline has a single stage named 'Test'.

3. **Test Stage:**
   - Inside the 'Test' stage, two steps are executed:
     - `node --version`: Prints the version of Node.js.
     - `echo "Task successful.....!!"`: Prints a success message.

## Author

[Sk Shamim Iqbal]
