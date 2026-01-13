pipeline {
    agent { label 'Java_Env' }

    stages {

        stage('Checkout') {
            steps {
                cleanWs()
                git branch: 'feature-1',
                    url: 'https://github.com/Mallesha3/parcel_service.git'
            }
        }

        stage('Build') {
            steps {
                sh '''
                    pwd
                    mvn clean install
                '''
            }
        }
    }
}
