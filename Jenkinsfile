pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh ' -o PES2UG20CS309-1 PES2UG20CS309.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './PES2UG20CS309-1'
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
