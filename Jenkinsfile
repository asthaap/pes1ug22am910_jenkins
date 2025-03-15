pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Compiling hello.cpp...'
                sh 'make -C main'  // Runs the Makefile inside the "main" directory
            }
        }

        stage('Test') {
            steps {
                echo 'Running the compiled executable...'
                sh './main/hello_exec'  // Runs the compiled executable
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
