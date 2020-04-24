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
                withSonarQubeEnv('sonar') {
                sh 'mvn sonar:sonar'
                }
            }
        }
    }
}
