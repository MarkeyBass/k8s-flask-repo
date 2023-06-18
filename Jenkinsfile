pipeline {
    agent any

    stages {
        stage('Flask deploy') {
          steps {
            sh  'kubectl apply -f flask-deployment.yaml'
          }
        }
        stage('Check Kubernetes data') {
            steps {
                sh 'kubectl get all --namespace flask-space'
            }
        }
    }
}