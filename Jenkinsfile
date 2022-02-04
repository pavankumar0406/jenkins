pipeline {
    agent any

    tools {
        maven 'Apache Maven 3.8.5'
    }

    stages {
        stage('Git clone ') {
        steps {
            git branch: 'main', credentialsId: 'pavan', url: 'https://github.com/pavankumar0406/app.git'
        }
        }

        stage('maven version') {
            steps {
              sh 'mvn -version'
        }
        }
        stage('maven clean') {
            steps {
              sh 'mvn clean'
        }
        }
        stage('sonar scan') {
            steps {
              sh 'mvn sonar:sonar -Dsonar.host.url=http://52.66.241.199:9000 -Dsonar.login=743e00dd89b6b8af30b65f713408fa6e0448d8f1'
        }
        }
        stage('maven validate') {
            steps {
              sh 'mvn validate'
        }
        }
        stage('maven compile') {
            steps {
              sh 'mvn compile'
        }
        }
        stage('mvn test') {
            steps {
              sh 'mvn test'
        }
        }
        stage('mvn package') {
            steps {
              sh 'mvn package'
        }
        }
        stage('mmvn deploy') {
            steps {
              sh 'mvn deploy'
        }
        }
    }
}
