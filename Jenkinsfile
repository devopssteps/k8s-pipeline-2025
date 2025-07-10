pipeline {
    agent any
    environment {
        DOCKER_IMAGE = 'devopssteps/laravel-app'
        IMAGE_TAG = 'latest'
        K8S_NAMESPACE = 'default'
        DOCKERHUB_CREDENTIALS = credentials('docker-hub-credential')
        KUBE_DEPLOYMENT_NAME = 'laravel-app'
        APP_LABEL = 'laravel'
        KUBECONFIG = "/var/lib/jenkins/kube-minikube/config"
        MINIKUBE_HOME = "/var/lib/jenkins/kube-minikube/.minikube"
    }
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t $DOCKER_IMAGE:$IMAGE_TAG .'
                
            }
        }
        stage('Push') {
            steps {
               sh 'echo image push stage' 
               
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo delpoy stage'
            }
        }
    }
}