pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Compiling main.cpp...'
                bat """
                    cd %WORKSPACE%
                    "C:\\MinGW\\bin\\gcc.exe" main.cpp -o hello.exe -lstdc++
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
