pipeline {
	agent {
	label "slave-1"
	}
	stages {
		stage ('deploy-index') {
		steps {
			sh "cp-r index.html/var/www/html"
			sh "chmod -R 777 /var/www/html"
			}
		}
	}
}
