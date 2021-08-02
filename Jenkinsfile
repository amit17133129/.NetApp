pipeline {
 agent any;
 environment {
    MSBUILD = "C:/Program Files (x86)/Microsoft Visual Studio/2019/Community/MSBuild/Current/Bin/MSBuild"
 
     
  }
  stages {
    stage('Build') {
      steps {
    
        bat "\"${MSBUILD}\" C:/Users/Administrator/source/repos/WebApplication4-7/WebApplication4-7"
      
      }
    }
  }
   post {  
             
         success {  
           mail bcc: '', body: 'Hey, .Net Applicationb sun successfully', cc: '', from: '', replyTo: '', subject: 'Job Succeeded', to: 'amitsharma13317@gmail.com'  
         }  
         failure {  
             mail bcc: '', body: 'Hey, .Net Application Failed', cc: '', from: '', replyTo: 'Job Failed', subject: '', to: 'amitsharma13317@gmail.com'
         }  
 }
}
