pipeline {
    agent any
    stages {
        stage('NPM Install') {
            steps {
                bat 'npm install'
            }
        }
        parallel {
            stage('Run npm Audit tests') {
                steps {
                    bat 'npm audit'
                }
            }
            stage('NPM Test') {
                steps {
                    bat 'npm test'
                }
            }
        }
    }
    // post {
    //     always {

    //     }
    // }
}