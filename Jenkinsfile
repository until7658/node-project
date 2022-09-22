pipeline {
    environment { 
        DOCKER_NAME = "node-project"  //docker hub id와 repository 이름
        DOCKER_VERSION = "0.0.1"
        dockerImage = '' 
    }
    agent any

    stages {
        stage('Create docker image') {
            steps {
                script {
                    dockerImage = docker.build DOCKER_NAME + ":" + DOCKER_VERSION + " ."
                }
            }
        }
    }
}
