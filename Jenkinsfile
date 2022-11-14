pipeline {
	agent {
		docker {
			image 'jenkins-blueocean'
		}
	}
	stages {
		stage('Build') {
			steps {
				sh 'composer install'
			}
		}
		stage('Test') {
			steps {
                sh './vendor/bin/phpunit tests'
            		}
		}
	}
}
