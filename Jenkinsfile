pipeline {
    agent any
    stages {
        stage('runfrontend') {
            steps {
                echo "frontend"
                nodejs('Node-10-17') {
                    sh 'yarn install'
                }
            }
        }
        stage('runbackend') {
            steps {
                echo "backend"
                    withGradle() {
                        sh './gradlew -v'
                    }
                }
            }
        }
    }
}