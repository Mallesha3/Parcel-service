pipeline{

agent any

stages{
stage('Checkout') {
            steps {
                sh 'rm -rf *'
               sh 'https://github.com/Mallesha3/parcel_service.git'
              
            }
   }
  stage('Build') {
            steps {
                    sh '''
                    cd parcel_service
                    git checkout feature-1
                    pwd
                    mvn clean install
                '''
            }
        }
}

}
