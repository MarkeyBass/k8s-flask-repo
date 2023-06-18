pipeline {
    agent any

    stages {
        stage('Build image') {
          steps {
            sh  'docker build -t flask-frontend:${params.flask_version} .'
          }
        }
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