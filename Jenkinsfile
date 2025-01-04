pipeline {
    agent any
    parameters {
        string(name: 'DOCKER_IMAGE', defaultValue: 'mariadb', description: 'Specify the Docker image to pull and run')
    }
    stages {
        stage('Pull and Run Docker Image') {
            steps {
                script {
                    sh "echo Using Docker Image: ${params.DOCKER_IMAGE}"
                    sh "docker pull ${params.DOCKER_IMAGE}"
                    sh "docker run ${params.DOCKER_IMAGE}"
                }
            }
        }
    }
}
