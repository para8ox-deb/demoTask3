pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/para8ox-deb/demoTask3.git'
            }
        }
        stage('Build') {
            steps {
                bat 'C:\\MinGW\\bin\\gcc.exe main.cpp -o hello.exe'
            }
        }
        stage('Execute') {
            steps {
                bat 'hello.exe'
            }
        }
    }
}
