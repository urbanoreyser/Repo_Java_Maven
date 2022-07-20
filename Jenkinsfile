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
                  sh 'mvn -B -DskipTests clean package'
            }
        }
             stage('Unit_testing') {
              steps {
                echo 'Testing'
                  sh 'mvn test'
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
