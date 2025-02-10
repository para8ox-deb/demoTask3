pipeline {
    agent any
    environment {
        PATH = "${env.PATH};C:\\MinGW\\bin"
    }
    stages {
        stage('Build') {
            steps {
                echo 'Compiling main.cpp...'
                bat """
                    gcc.exe main.cpp -o hello.exe -lstdc++
                """
            }
        }
        stage('Execute') {
            steps {
                echo 'Running hello.exe...'
                bat 'hello.exe'
            }
        }
    }
    post {
        failure {
            echo 'Build failed. Check the build log for details.'
        }
    }
}
