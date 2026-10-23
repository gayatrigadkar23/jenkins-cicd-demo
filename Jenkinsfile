
pipeline {
    agent any

    environment {
        IMAGE_NAME = 'jenkins-cicd-demo'
        CONTAINER_NAME = 'jenkins-demo-app'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the application Docker image...'
                bat '"C:\\Users\\hp\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker.exe" build -t jenkins-cicd-demo .'
            }
        }

        stage('Test') {
            steps {
                echo 'Checking Docker image...'
                bat '"C:\\Users\\hp\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker.exe" images jenkins-cicd-demo'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application container...'
                bat '"C:\\Users\\hp\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker.exe" rm -f jenkins-demo-app'
                bat '"C:\\Users\\hp\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker.exe" run -d --name jenkins-demo-app -p 3000:3000 jenkins-cicd-demo'
            }
        }
    }
}
