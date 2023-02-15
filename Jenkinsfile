pipeline {

  agent any
stages {
  
  stage('---clean---'){
    steps{
      script{
    //sh "mvn clean"
      echo "Clean phase Febrero"
      print "Clean Febrero"
      }
      }
  }
  
    stage('---Credentials---'){
    steps{
withCredentials([usernamePassword(credentialsId: id, usernameVariable: 'username', passwordVariable: 'password')]) {
     
  print "${username}"
  print "${password}"
}
    }
  }
  
    stage('---package---'){
    steps{
   // sh "mvn package"
    echo "Package phase"
    }
  }
  
}
  
  }
