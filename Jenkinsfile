pipeline {
    node('master) {
    	stage('build') {
            	echo 'Build Project'
                sh 'mvn -B -DskipTests clean package'
	}
    }	
}
