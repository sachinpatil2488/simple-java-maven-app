node('master') {
    stage('checkout') {
    	checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/harshuk08/simple-java-maven-app.git']]])
    }
    stage('setup') {
	sh 'export M2_HOME=/opt/maven'
	sh 'export MAVEN_HOME=/opt/maven'
	sh 'export PATH=${M2_HOME}/bin:${PATH}'
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
