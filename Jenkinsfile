pipeline {
    agent any
    stages {
        stage('Initializing') {
            steps{
                script{
                    sh 'curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl" && chmod +x kubectl'
                }
            }
        }    
        stage('Orchestrate') {
           steps{
               script{
                   sh './kubectl create -f mywebapp.yaml'
               }
           }
        }
    }
}
