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
                    def dockerImage = "mpmanthan/firstimage"
                    def dockerTag = "v1"
                    def registryUrl = "https://hub.docker.com/"
                    def dockerCredentialsId = "Docker-cred"
                    // starting build process
                    def dockerBuild = docker.build("${dockerImage}:${dockerTag}",'.')
                    
                }
            }
        }
    }
}
