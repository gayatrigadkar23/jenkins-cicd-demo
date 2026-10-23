pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                bat 'docker --version'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing Docker...'
                bat 'docker run --rm hello-world'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment stage completed.'
            }
        }
    }
}
