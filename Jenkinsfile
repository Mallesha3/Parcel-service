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
        
//         stage('Run App (5 min)') {
//     steps {
//         timeout(time: 5, unit: 'MINUTES') {
//             sh '''
//                 java -jar target/simple-parcel-service-app-1.0-SNAPSHOT.jar
//             '''
//         }
//     }
// }
         stage('Build') {
            steps {
                sh '''
                    mvn clean deploy
                '''
            }
        }

    }
}
