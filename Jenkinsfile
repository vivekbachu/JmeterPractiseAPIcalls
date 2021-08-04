pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh docker run justb4/jmeter
                 }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}