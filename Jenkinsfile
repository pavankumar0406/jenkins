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
        stage('mvn Delpoy') {
            steps {
              sh 'mvn Delpoy'
        }
        }
    }
}
