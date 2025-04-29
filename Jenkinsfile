pipeline {
    agent any
    stages{
        stage('run frontend'){
            steps{
                echo 'frontend'
                nodejs('node-10-17') {
                    sh 'yarn install'                      
                }
            }
        }
        stage('run backend'){
            steps{
                echo 'backend'
                withGradle() {
                    sh './gradlew -v'                      
                }
            }
        }
    }
}