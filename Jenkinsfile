pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file using a shell script
                    sh 'g++ -o my_program my_program.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Print the output of the compiled program
                    sh './my_program'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // In a real-world scenario, you might deploy your application here
                    echo 'Deployment steps go here'
                }
            }
        }
    }

    post {
        always {
            // Display 'pipeline failed' in case of any errors within the pipeline
            echo 'Pipeline failed'
        }
    }
}
