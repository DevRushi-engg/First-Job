pipeline {
    agent any
    stages {
        stage('Build') {
            steps { echo 'Building' }
        }
        stage('Test') {
            parallel {
                stage('Unit') { 
                    steps { 
                        sh 'echo Unit test' 
                    } 
                }
                stage('Integration') {
                    steps { 
                        sh 'echo Integration tests'
                    }
                }
            }
        }
    }
}
                                            
