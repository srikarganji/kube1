pipeline {
    agent any 

    stages {
        stage('Build') {
            steps {
                script {
                    // Build your Docker image
                    bat 'docker build -t my-kube2 .'
                     bat 'docker tag my-kube2:latest srikarganji/my-kube2:latest'
                      bat 'docker push srikarganji/my-kube2:latest'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Run tests here if you have any
                    echo 'Running tests...'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    // Deploy your Docker image
                    echo 'Deploying application...'
                }
            }
        }
    }
}
