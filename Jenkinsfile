node {
    stage('========== Clone repository ==========') {
        checkout scm
    }
    stage('========== create docker image ==========') {
        app = docker.build("${env.IMAGE_NAME}:${env.IMAGE_VERSION}")
    }
    stage('========== docker tag ==========') {
        app = docker.tag("${env.IMAGE_NAME}:${env.IMAGE_VERSION} ${env.IMAGE_NAME}:latest")
    }
}