pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh ' -o PES2UG20CS309-1 PES2UG20CS309-1.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './PES2UG20CS309-1'
            }
        }
        stage('Deploy') {
            steps {
                // Add your deployment steps here
            }
        }
    }
    post {
        always {
            script {
                if (currentBuild.result == 'FAILURE') {
                    echo 'pipeline failed'
                }
            }
        }
    }
}
