pipeline {
    agent any
    stages {
        stage('Orchestrate') {
           steps{
               script{
                   sh 'kubectl apply -f mywebapp.yaml'
               }
           }
        }
    }
}
