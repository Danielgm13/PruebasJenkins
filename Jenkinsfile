pipeline {

  agent any

  parameters{
    text(name: 'nombre', description: 'nombre', defaultValue: 'nombre')
    string(name:'apellidos', description: 'apellidos', defaultValue: 'apellidos')
    string(name: 'pipeline', description: 'pipeline to execute', defaultValue: 'Pipeline SCM3')
    choice(name: 'edad', description: 'edad', choices: '16\n17\n18')
  }

  stages{

    stage("Invoce an other pipeline") {

      steps{

      script{

        build = build job: "${pipeline}",
        parameters: [
          text(name: 'nombre',value: 'nombrepipe')
          string(name:'apellidos', value: 'apellidos'pipe)
          choice(name: 'edad', value: '18')
        ],
        propagate: false

        build_result = "${build.getResult()}"
        print("Salida: ${build_result}")




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
