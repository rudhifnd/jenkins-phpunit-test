pipeline {
    agent {
        any {
            image 'composer:latest'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'composer.json install'
            }
        }
        stage('Test') {
            steps {
                sh './vendor/bin/phpunit tests'
            }
        }
    }
}
