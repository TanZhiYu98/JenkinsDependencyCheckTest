pipeline {
	agent {
		docker {
			image 'myjenkins-blueocean:2.361.2-1'
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
