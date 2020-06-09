pipeline {
	agent any

	options {
		buildDiscarder(logRotator(numToKeepStr: '10'))
	}



	stages {
        stage('Build') {
            steps {
              sh 'python --version'		
	      cmakeBuild
              generator: 'Unix Makefiles',
              buildDir: 'build',
              sourceDir: 'CFirst',
              installation: 'InSearchPath',
              steps: [
          	[args: 'all install', envVars: 'DESTDIR=${WORKSPACE}/artifacts']
              ]

            }
        }
	}
}
