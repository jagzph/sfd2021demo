pipeline {
    agent any
    stages {
        stage('Orchestrate') {
           steps{
               script{
                   sh '/usr/local/bin/kubectl/kubectl apply -f mywebapp.yaml'
               }
           }
        }
    }
}
