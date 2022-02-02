node {
    
    stage('Git clone ') {
        git branch: 'main', credentialsId: 'pavan', url: 'https://github.com/pavankumar0406/app.git'
    }
    stage ('mvn clean') {
        sh 'mvn clean'
    }
    stage ('mvn version') {
        sh 'mvn version'
    }
    stage ('mvn validate') {
        sh 'mvn validate'
    }
    stage ('sonar scan') {
        sh 'mvn sonar:sonar -Dsonar.host.url=http://13.233.78.227:9000 -Dsonar.login=743e00dd89b6b8af30b65f713408fa6e0448d8f1'
    }
    stage ('mvn compile') {
        sh 'mvn compile'
    }
    stage ('mvn test') {
        sh 'mvn test'
    }
    stage ('mvn package') {
        sh 'mvn package'
    }
    stage ('mvn Delpoy') {
        sh 'mvn deploy'
    }
}
