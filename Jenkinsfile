pipeline {
	agent {
	label "slave-1"
	}
	stages {
		stage ('deploy-index') {
		steps {
			sh "cd /var/lib/docker"
			sh "docker run -itd --name slave-container saraswatiwalave/my-ubuntu:2.0"
			sh "docker cp index.html slave-container:/var/www/html/"
			sh "chmod -R 777 /var/www/html"
			}
		}
	}
}
