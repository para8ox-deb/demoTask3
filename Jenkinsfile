pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Compiling main.cpp...'
                bat 'C:\\MinGW\\bin\\gcc.exe main.cpp -o hello.exe -lstdc++'
            }
        }
        stage('Execute') {
            steps {
                echo 'Executing hello.exe...'
                bat 'hello.exe'
            }
        }
    }
    post {
        success {
            echo 'Build and execution successful!'
        }
        failure {
            echo 'Build failed. Please check for errors in main.cpp or GCC configuration.'
        }
    }
}
