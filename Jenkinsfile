pipeline {

  agent any

  parameters{
    text(name: 'nombre', description: 'nombre', defaultValue: 'nombre')
    string(name:'apellidos', description: 'apellidos', defaultValue: 'apellidos')
    string(name: 'pipeline', description: 'pipeline to execute', defaultValue: 'pipeline')
    choice(name: 'edad', description: 'edad', choices: '16\n17\n18')
  }

  stages{

    stage("Invoce an other pipeline") {

      steps{

      script{

        print("${env.pipeline}")
        build = build job: "${env.pipeline}",
        parameters: [
          text(name: 'nombre',value: 'nombrepipe'),
          string(name:'apellidos', value: 'apellidospipe')
        ],
        propagate: false

        build_result = "${build.getResult()}"
        print("Salida: ${build_result}")
        
        variable_results = build.getBuildVariables();
        
        saludo = variable_results.saludo
        
        print("${saludo}")
        




          } // END Scripts
      } // END Streps
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
