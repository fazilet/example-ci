pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
			sh 'ls'
			npm install
			npm install grunt-cli
			./node_modules/grunt-cli/bin/grunt
			}
		}
		stage ('Packaging') {
			tar cfz website.tgz _less.github.io
		}
	}	
	post {
		always {
			archiveArtifacts artifacts: 'path/to/*.jar',
			fingerprint: true
		}
	}	
}
