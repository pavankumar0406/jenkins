pipeline {
    agent any

    tools {
        maven 'Apache Maven 3.0.5'
    }

    stages {
        stage('Git clone ') {
        steps {
            git branch: 'main', credentialsId: 'git-cred', url: 'https://github.com/pavankumar0406/app.git'
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
              sh 'mvn sonar:sonar -Dsonar.host.url=http://34.125.153.241:9000 -Dsonar.login=0dd574497075c4de7e94ebf459aab051167465d5'
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
        stage('mvn deploy') {
            steps {
              sh 'mvn deploy'
        }
        }
    }
}
