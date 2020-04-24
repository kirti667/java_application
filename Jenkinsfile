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
                withSonarQubeEnv('sonarQube') {
                            sh 'mvn sonar:sonarQube'
                }
            }
        }
    }
}
