pipeline {
    agent any
    environment {
        NODE_VERSION = '16'  // Specify Node.js version
        IMAGE_NAME = 'jaggi/cicd_lab_2'  // Docker image name
    }
    triggers {
        pollSCM('H/5 * * * *') // Poll every 5 minutes for changes
    }
    stages {
        stage('Checkout') {
            steps {
                // Cloning the GitHub repository with credentials
                git(
                    branch: 'main',
                    url: '
                  https://github.com/jagjeetsinghsandhu22129/cicd_lab_2.git'
,
                    credentialsId: 'JJ'
                )
            }
        }
          stage('Build') {
            steps {
                echo 'Building the application..........'
                // Add any build commands here
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests.........'
                // Add test commands or scripts here
            }
        }
    }
    post {
        success {
            echo 'Build and tests succeeded!!!!!!!!'
        }
        failure {
            echo 'Build or tests failed........'
        }
    }
}
