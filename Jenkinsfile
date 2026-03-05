pipeline {
    agent any

    stages {

        stage('Check Kubernetes') {
            steps {
                sh 'kubectl get nodes'
            }
        }

        stage('Deploy Pod') {
            steps {
                sh 'kubectl apply -f pod.yaml'
            }
        }

        stage('Verify') {
            steps {
                sh 'kubectl get pods'
            }
        }
    }
}
