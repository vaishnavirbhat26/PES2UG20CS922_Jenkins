pipeline {
    agent any

stages{
  stage('Build') {
    steps{
        sh 'g++ -o PES2UG20CS922 PES2UG20CS922.cpp'
    }
  }

  stage('Test') {
    steps{
       sh './PES2UG20CS922'
    }
  }

  stage('Deploy') {
    steps{
      echo 'DEPLOYMENT SUCCESSFUL FROM GITHUB REPO - PES2UG20CS922_Jenkins'
    }
  }
}
post {
    always {
      echo 'Pipeline was completed'
    }
    failure {
        echo 'Pipeline has Failed'
    }
  }
}
