pipeline {
	agent any

	options {
		buildDiscarder(logRotator(numToKeepStr: '10'))
	}



	stages {
        stage('Build') {
            steps {
              generator('Unix Makefiles')
              cleanBuild()		
              buildDir(build)
              sourceDir(CFirst)
              cmakeBuild(
            	installation: 'InSearchPath'
              )
              
        }
	}
}
}
