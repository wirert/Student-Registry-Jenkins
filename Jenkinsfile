pipeline {
    agent any
    stages {
        stage('NPM Install') {
            steps {
                bat 'npm install'
            }
        }
        stage('NPM Test') {
            steps {
                bat 'npm test'
            }
        }
    }
    // post {
    //     always {

    //     }
    // }
}