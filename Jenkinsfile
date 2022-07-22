pipeline {
    agent any

    stages {
        stage('Git checkout code') {
            steps {
                echo 'Git checkout'
                sh 'pwd'
                sh 'ls'
            }
        }
            stage('Build') {
              steps {
                echo 'Building'
                  sh 'mvn -B -DskipTests clean package'
            }
        }
             stage('Unit_testing') {
              steps {
                echo 'Testing'
                  sh 'mvn test'
            }
        }
            stage('SonarQube_analysis') {
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
