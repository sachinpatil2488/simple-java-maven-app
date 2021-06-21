node('master') {
    stage('checkout') {
    	checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/harshuk08/simple-java-maven-app.git']]])
    }
    stage('clean') {
	sh 'mvn clean'
    }
    stage('build') {
	sh 'mvn compile'
	sh 'mvn test'
	sh 'mvn package'
    }
}
