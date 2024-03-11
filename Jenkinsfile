pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file using a shell script
                    build 'PES2UG21CS180-1'
                    sh 'g++ main1.cpp -o output'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Print the output of the compiled program
                    sh './output'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // In a real-world scenario, you might deploy your application here
                    echo 'deploy'
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
