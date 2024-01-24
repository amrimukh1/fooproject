pipeline {
  agent any 
  environment{
    def myString = 'https://github.com/amrimukh1/fooproject.git'
    def myString1 = "mvn compile"
    def myString2 = "mvn test"
    def myString3 = '**/TEST*.xml'
  }
  
  stages {
    stage('Checkout') {
      steps {
        git ${myString}
      }
    }  
    
    stage('Build') {
      steps {
        sh ${myString1}
      }
    }  
    stage('Test') {
      steps {
        sh ${myString2}
      }
     post {
      always {
        junit ${myString3}
      }
     }
  }
 }
}
