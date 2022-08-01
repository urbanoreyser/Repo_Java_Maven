pipeline {
    agent any

    stages {
        stage('Git checkout') {
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
                  stage("Quality Gate") {
              steps {
                timeout(time: 1, unit: 'HOURS') {
                waitForQualityGate abortPipeline: true
                echo 'Quality Gate'
           }
        }
    }
}
