pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Compile the .cpp file using a shell script
                build 'PES2UG21CS468-1'
                sh 'g++ -o PES2UG21CS468-1 hello.cpp'
            }
        }

        stage('Test') {
            steps {
                // Print the output of the compiled .cpp file
                sh './PES2UG21CS468-1'
            }
        }

        stage('Deploy') {
            steps {
              echo 'deploy'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
