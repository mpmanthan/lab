pipeline {
    agent any 

    stages {
        stage('go to git') {
            steps {
                // checkout Git repo
                checkout scm
            }
        }
        stage('Build and push') {
            steps {
                script {
                    // Docker image and tags
                    def dockerImage = "mpmanthan/sisl"
                    def dockerTag = "v1"
                    def dockerCredentialsId = "Docker-cred"
                    // starting build process
                    def dockerBuild = docker.build("${dockerImage}:${dockerTag}",'.')
                }
            }
        }
    }
}
