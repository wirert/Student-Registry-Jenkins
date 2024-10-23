pipeline {
    agent any
    stages {
        stage('NPM Install') {
            steps {
                bat 'npm install'
            }
        }
        stage('Run parallel tests') {
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
        stage('Deploy to Staging') {
            echo 'Deploy to Staging'
        }
        stage('Approval for Prod deploy') {
            steps {
                input message: 'Approve deployment to production?', ok: 'Deploy'
            }
        }
        stage('Deploy to Production') {
            echo 'Deploy to Production'
        }
    }
    // post {
    //     always {

    //     }
    // }
}