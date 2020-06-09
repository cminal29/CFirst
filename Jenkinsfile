pipeline {
	agent any

	options {
		buildDiscarder(logRotator(numToKeepStr: '10'))
	}



	stages {
        stage('Build') {
            steps {
              generator: 'Unix Makefiles',
              cleanBuild(),		
              buildDir: 'build',
              sourceDir: 'source',
              installation: 'InSearchPath',
              steps: [
          [args: 'all install', envVars: 'DESTDIR=${WORKSPACE}/artifacts']
      ]
            }
        }
	}
}
