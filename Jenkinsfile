node {

    stage('Checkout') {
        checkout scm
    }

    stage('Test') {
        sh 'test -f index.html'
        echo 'HTML application test passed'
    }

    stage('Docker Build') {
        sh 'docker build -t exp6-html:v1 .'
        sh 'minikube image load exp6-html:v1'
    }

    stage('Kubernetes Deploy') {
        sh 'kubectl apply -f deployment.yaml'
        sh 'kubectl apply -f service.yaml'
    }

    stage('Verify') {
        sh 'kubectl get deployments'
        sh 'kubectl get pods'
        sh 'kubectl get services'
    }

    echo 'DevOps pipeline completed successfully!'
}
