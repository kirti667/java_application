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
                with SonarQubeEnv ('sonar') {
                sh 'mvn sonar: sonar'
                }
            }
        }
    }
}
