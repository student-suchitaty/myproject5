
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Source code is available in the workspace'
            }
        }

        stage('Build') {
            steps {
                sh 'echo Building application'
                sh 'mkdir -p output'
                sh 'echo Build completed > output/build.txt'
            }
        }

        stage('Test') {
            steps {
                sh 'test -f output/build.txt'
                echo 'Basic test passed'
            }
        }

        stage('Package') {
            steps {
                sh 'tar -czf application-artifact.tar.gz output'
            }
        }
    }
}
