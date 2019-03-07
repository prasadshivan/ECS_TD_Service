pipeline {
  agent any
  stages {
    stage('Register new Task Defenition') {
      steps {
        sh 'aws ecs register-task-definition --cli-input-json file://task_definition.json' 
      }
    }
   
   stage('Update a Service') {
      steps {
        sh 'aws ecs update-service --cluster DevopsTest --service ecs-simple-service2 --task-definition ExampleTask --desired-count 3'
      }
    }
   
    }
}
