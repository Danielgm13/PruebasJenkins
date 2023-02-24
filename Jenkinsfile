pipeline {

  agent any
  
  parameters{
    text(name: 'nombre', description: 'nombre', defaultValue: 'nombre')
    string(name:'apellidos', description: 'apellidos', defaultValue: 'apellidos')
    choice(name: 'edad', description: 'edad', choices: '16\n17\n18')
  }
  
  stages{
  
    stage("Saludo") {
      
      steps{
    
      script{
        retryCount = 0
        
        retry (3){
          
        retryCount = retryCount +1
        echo "Saludo echo"
        print "Saludo print"
         
          if (retryCount < 3){
            error("Error compañero")
          }
        }
          }
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
