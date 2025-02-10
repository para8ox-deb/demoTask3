pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'C:\\MinGW\\bin\\gcc.exe main.cpp -o hello.exe' // Correct path to gcc
            }
        }
        stage('Execute') {
            steps {
                bat 'hello.exe'  // Assumes hello.exe is in the workspace after build
            }
        }
    }
}
