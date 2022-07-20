pipeline {
    agent any

    stages {
        stage('git checkout') {
            steps {
                echo 'Git checkout jenkins'
                sh 'pwd'
                sh 'ls'
            }
        }
            stage('build') {
              steps {
                echo 'Building'
            }
        }
             stage('Unit_testing') {
              steps {
                echo 'Testing'
            }
        }
            stage('SonarQube') {
              steps {
                echo 'Sonar'
            }
        }
            stage('Deploy to Dev') {
              steps {
                echo 'Deployment'
            }
        }
    }
}
