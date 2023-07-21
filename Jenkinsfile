pipeline {
	agent {
	label "slave-1"
	}
	stages {
		stage ('deploy-index') {
		steps {
			sh "docker run -itd --name slave-container my-ubuntu:2.0"
			sh "docker cp index.html slave-container:/var/www/html/"
			sh "chmod -R 777 /var/www/html"
			}
		}
	}
}
