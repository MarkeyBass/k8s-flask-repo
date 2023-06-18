pipeline {
    agent any

    stages {
        stage('Check Kubernetes') {
            steps {
                sh 'kubectl get all --namespace flask-space'
            }
        }
        stage('Flask deploy') {
          steps {
            sh  'kubectl apply -f flask-deployment.yaml'
          }
        }
    }
}