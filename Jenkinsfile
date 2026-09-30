@Library('jenkins-demo') _

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                mavenBuild()
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }

    post {
        always {
            cleanWs()
        }
    }
}
