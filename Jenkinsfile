pipeline {
    agent any
    parameters {
        choice(name: 'ENVIRONMENT', choice: ['staging', 'production'], description: 'Target')
    }
    stages {
        stage('Deploy') {
            steps {
                sh "echo Deploying to ${params.ENVIRONMENT}"
            }
        }
    }
}
