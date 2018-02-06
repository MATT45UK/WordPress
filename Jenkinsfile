pipeline {
    agent any

    stages {
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
