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
                withSonarQubeEnv('sonar-key') {
                sh 'mvn sonar:sonar'
                }
            }
        }
    }
}
