pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                sh 'mvn clean package'
        }
        }
        stage('SonarQube Analysis') { 
            steps {
                withSonarQubeEnv('sonar working token') {
                sh 'mvn sonar:sonar working token'
                }
            }
        }
    }
}
