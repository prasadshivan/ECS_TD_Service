pipeline {
  agent any
  stages {
    stage('Register new Task Defenition') {
      steps {
        sh 'aws ecs register-task-definition --cli-input-json file://task_definition.json --tags key=stack,value=dev' 
      }
    }
   
   stage('create a new service') {
      steps {
        sh 'aws ecs create-service --cluster DevopsTest --service-name ecs-simple-service2 --task-definition ExampleTask --desired-count 3'
      }
    }
   
    }
}
