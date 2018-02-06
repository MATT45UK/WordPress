pipeline {
    agent any

    stages {
        stage('Checkout') {
	    steps {
		checkout scm
	    }
	}
	stage('Build') {
            steps {
                echo 'Building..'
		app = docker.build(webserver)
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
