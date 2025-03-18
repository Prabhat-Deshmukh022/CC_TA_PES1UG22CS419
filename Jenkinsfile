pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo "Compiling C++ program..."
                    sh 'g++ -o hello_exec hello.cpp'
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    echo "Running the program..."
                    sh './hello_exec'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo "Deployment successful (placeholder stage)."
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
