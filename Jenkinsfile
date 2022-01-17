node {
    
    stage('Git clone ') {
        git branch: 'main', credentialsId: 'pavan', url: 'https://github.com/pavankumar0406/app.git'
    }
    stage ('mvn clean') {
        sh 'mvn clean'
    }
    stage ('mvn validate') {
        sh 'mvn validate'
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
