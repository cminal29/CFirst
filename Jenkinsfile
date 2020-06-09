pipeline {
	agent any

	options {
		buildDiscarder(logRotator(numToKeepStr: '10'))
	}



	stages {
        stage('Build') {
            steps {
                cmakeBuild(
	        	installation: 'InSearchPath'
              )
              
        }
	}
}
}
