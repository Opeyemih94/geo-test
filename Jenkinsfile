 pipeline{
    agent any 
    stages {
        stage('maven clean'){
        steps{
            sh '/opt/maven/bin/mvn clean'
            sh 'mvn clean'
        }
    }    
    stage('maven install'){
          steps{
            sh '/opt/maven/bin/mvn clean'
          sh 'mvn install'
          sh 'echo hi'
          }
    }        
              
    }        
 }        
    

