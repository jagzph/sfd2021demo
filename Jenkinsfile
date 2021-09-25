pipeline {
    agent any
    stages {
        stage('Initializing') {
            steps{
                script{
                    sh 'curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl" && chmod +x kubectl'
                    sh 'curl -o aws-iam-authenticator https://amazon-eks.s3.us-west-2.amazonaws.com/1.21.2/2021-07-05/bin/linux/amd64/aws-iam-authenticator && chmod +x aws-iam-authenticator'
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
