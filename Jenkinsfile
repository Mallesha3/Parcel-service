pipeline{

agent any

stages{
stage('Checkout') {
            steps {
                sh 'rm -rf *'
               sh 'git clone https://github.com/Mallesha3/Parcel-service.git'
              
            }
   }
  stage('Build') {
            steps {
                    sh '''
                    cd Parcel-service
                    git checkout feature-1
                    pwd
                    mvn clean install
                '''
            }
        }
}

}
