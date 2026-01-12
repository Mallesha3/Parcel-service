pipeline{

agent any

stages{
stage('Checkout') {
            steps {
                sh 'rm -rf *'
               sh 'git clone https://github.com/Mallesha3/Parcel-service.git'
              sh 'cd Parcel-service'
              sh 'git checkout feature-1'
              
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
