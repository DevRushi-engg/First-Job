pipeline {
    agent any
    parameters {
        choice(name: 'ENVIRONMENT', choices: ['staging', 'production'], description: 'Target')
    }
    stages {
        stage('Test') {
            parallel {
                stage('Unit') {
                    steps {
                        sh 'echo Unit tests'
                    }
                }
                stage('Integration') {
                    steps {
                        sh 'echo Integration test'
                    }
                }
            }
        }
        
        stage('Deploy') {
            steps {
                sh "echo Deploying to ${params.ENVIRONMENT}"
            }
        }
    }
}
