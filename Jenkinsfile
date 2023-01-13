pipeline {
  agent any
  tools {
    maven 'Maven'
  }
  stages {
    stage ('Initialize') {
      steps {
        sh '''
                echo "PATH = ${PATH}"
                echo "M2_HOME = ${M2_HOME}"
           '''
      }
    }
           
           stage ('Build'){
             steps{
             sh 'mvn clean package'
             sh ' cp /var/lib/jenkins/workspace/webapp-cicd-pipeline/target/WebApp.war /prod/apache-tomcat-10.0.27/webapps'
           }
             
         
          }
  }
  }
