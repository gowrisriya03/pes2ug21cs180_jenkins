pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file
                    sh 'g++ main1.cpp -o output'
                    // Archive the compiled binary as an artifact
                    archiveArtifacts artifacts: 'output', fingerprint: true
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
                    // Placeholder for deployment steps
                    echo 'Deploying...'
                }
            }
        }
    }

    post {
        failure {
            // Display 'pipeline failed' only in case of failure
            echo 'Pipeline failed'
        }
    }
}
