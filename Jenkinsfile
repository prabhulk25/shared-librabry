pipeline{
  agent any //{label 'node_name'}
  stages{
    stage("Cloning the Project"){
      steps{
      git url: 'https://github.com/prabhulk25/shared-librabry.git' branch: 'main'
      }
    }
    stage("Login to dockerhub"){
      steps{
        withCredentials([usernamePassword(credentialsId:'id',
          usernameVariable: 'username',passwordVariable: 'pass')]){
          sh 'docker login -u "${username}" -p "${pass}"'
          }
      }
    }
    stage("Build image"){
      steps{
      sh 'docker build -t image-name .'
    }
  }
}
