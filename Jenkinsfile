pipeline 
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o hello_exec main.cpp'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh './hello_exec'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Application...'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
