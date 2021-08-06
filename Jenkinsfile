pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            agent {
                docker { image 'justb4/jmeter' }
            }

            steps {
                echo 'Testing..'
                sh 'docker run -v /Users/vivekbachu/jenkins_data_new/workspace/jenkinsfiletriggerpipeline:/hello justb4/jmeter -n -t /hello/GetRecordAPI.jmx -JRESPONSEOUTPUT=/hello/Response.csv -JUser=1 -JLoopCount=1'
                    
                 }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
