pipeline {
    agent any
    stages {
        stage('NPM Install') {
            steps {
                bat 'npm install'
            }
        }
        stage('Parallel Execution') {
            parallel {
                stage('Run npm audit tests') {
                    steps {
                        bat 'npm install'
                    }
                }
                stage('Execute tests') {
                    steps {
                        bat 'npm test'
                    }
                }
            }
        }
    }
}