 pipeline{
    agent any
    tools{
        maven 'M2_HOME'
    } 
    stages {
        stage('maven clean'){
        steps{
            sh 'mvn clean'
        }
    }    
    stage('maven install'){
          steps{
          sh 'mvn install'
          sh 'echo hi'
          }
    }        
    stage('upload artifact'){
        steps{
          nexusArtifactUploader artifacts: [[artifactId: 'target/bioMedical-0.0.2-SNAPSHOT.jar',
           classifier: '', file: 'target/bioMedical-0.0.2-SNAPSHOT.jar',
            type: 'jar']], credentialsId: 'NexusID', groupId: 'qa',
             nexusUrl: '198.58.119.40:8081/',
              nexusVersion: 'nexus3',
               protocol: 'http',
               repository: 'suliyat', 
               version: '002'
        }
     } 

    }        
         
    

