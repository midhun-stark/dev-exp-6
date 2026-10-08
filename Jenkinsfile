pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Test') {
            steps {
                sh 'test -f index.html'
                echo 'HTML application test passed'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t exp6-html:v1 .'
                sh 'minikube image load exp6-html:v1'
            }
        }

        stage('Kubernetes Deploy') {
            steps {
                sh 'kubectl apply -f deployment.yaml'
                sh 'kubectl apply -f service.yaml'
            }
        }

        stage('Verify') {
            steps {
                sh 'kubectl get deployments'
                sh 'kubectl get pods'
                sh 'kubectl get services'
            }
        }
    }

    post {
        success {
            echo 'DevOps pipeline completed successfully!'
        }

        failure {
            echo 'DevOps pipeline failed!'
        }
    }
}pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Test') {
            steps {
                sh 'test -f index.html'
                echo 'HTML application test passed'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t exp6-html:v1 .'
                sh 'minikube image load exp6-html:v1'
            }
        }

        stage('Kubernetes Deploy') {
            steps {
                sh 'kubectl apply -f deployment.yaml'
                sh 'kubectl apply -f service.yaml'
            }
        }

        stage('Verify') {
            steps {
                sh 'kubectl get deployments'
                sh 'kubectl get pods'
                sh 'kubectl get services'
            }
        }
    }

    post {
        success {
            echo 'DevOps pipeline completed successfully!'
        }

        failure {
            echo 'DevOps pipeline failed!'
        }
    }
}pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Test') {
            steps {
                sh 'test -f index.html'
                echo 'HTML application test passed'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t exp6-html:v1 .'
            }
        }

        stage('Kubernetes Deploy') {
            steps {
                sh 'kubectl apply -f deployment.yaml'
                sh 'kubectl apply -f service.yaml'
            }
        }

        stage('Verify') {
            steps {
                sh 'kubectl get deployments'
                sh 'kubectl get pods'
                sh 'kubectl get services'
            }
        }
    }

    post {
        success {
            echo 'DevOps pipeline completed successfully!'
        }

        failure {
            echo 'DevOps pipeline failed!'
        }
    }
}
