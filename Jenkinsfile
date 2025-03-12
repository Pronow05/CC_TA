pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o hello_exec hello.cpp'  // Compile C++ file
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './hello_exec'  // Run the compiled executable
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment step - Placeholder for actual deployment'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
