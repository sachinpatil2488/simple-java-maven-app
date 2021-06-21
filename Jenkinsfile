pipeline {
  agent any
  
  stages {
    stage('Build and Test') {
      parallel {

        stage('Compile On Slave 1') {
          agent {
            node {
              label 'slave-1'
            }
          }
          steps {
            sh "mvn clean"
          }
        }
        stage('build On Slave 1') {
          agent {
            node {
              label 'slave-1'
            }
          }
          steps {
            	sh 'mvn compile'
				sh 'mvn test'
				sh 'mvn package'
          }
        }
        stage('Compile On Slave 2') {
          agent {
            node {
              label 'slave-2'
            }
          }
          steps {
            sh "mvn clean"
          }
        }
        stage('build On Slave 2') {
          agent {
            node {
              label 'slave-2'
            }
          }
          steps {
            	sh 'mvn compile'
				sh 'mvn test'
				sh 'mvn package'
          }
        }

      }
    }

  }
}
