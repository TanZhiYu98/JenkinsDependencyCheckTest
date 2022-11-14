pipeline {
	agent {
		docker {
			image 'myjenkins-blueocean'
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
