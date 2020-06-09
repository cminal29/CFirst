pipeline {
	agent any

	options {
		buildDiscarder(logRotator(numToKeepStr: '10'))
	}



	stages {
        stage('Build') {
            steps {
                cmakeBuild(
	      generator('Unix Makefiles')
              buildDir(build)
              sourceDir(CFirst)
            	installation: 'InSearchPath'
              )
              
        }
	}
}
}
