pipeline {
	agent {
	label "slave-1"
	}
	stages {
		stage ('deploy-index') {
		steps {
			sh "yum install docker -y"
			sh "systemctl start docker"
			sh "yum install httpd -y"
			sh "service httpd start"
			sh "docker run -itd --name slave-container my-ubuntu:1.0 bash"
			sh "docker cp index.html slave-container:/var/www/html/"
			sh "chmod -R 777 /var/www/html"
			}
		}
	}
}
