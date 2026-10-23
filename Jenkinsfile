pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                bat '"C:\\Users\\hp\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker.exe" --version'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing Docker...'
                bat '"C:\\Users\\hp\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin\\docker.exe" run --rm hello-world'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment stage completed.'
            }
        }
    }
}
