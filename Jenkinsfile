pipeline {
    agent any

    stages {
        stage('Check Kubernetes') {
            steps {
                sh 'kubectl get all --namespace flask-space'
            }
        }
    }
}