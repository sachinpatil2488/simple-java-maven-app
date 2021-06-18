node('master') {
    stage('checkout') {
    	checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/sachinpatil2488/simple-java-maven-app.git']]])
    }
    stage('clean') {
	sh 'mvn clean'
    }
    stage('compile') {
	sh 'mvn compile'
    }
    stage('test') {
	sh 'mvn test'
    }
    stage('package') {
	sh 'mvn package'
    }
}
