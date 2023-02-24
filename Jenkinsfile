pipeline {

  agent any
  
  stages{
  
    stage("Saludo") {
    
      script{
        echo "Saludo echo"
        print "Saludo print"
      }
    } // END Stage Saludo
  
  
  }
  post {
  
    success { 
      echo "Success"
    }
    
    failure {
      echo "Failure"
    }
    
    aborted {
      echo "Aborted"
    }
  
  }
  
  
}
