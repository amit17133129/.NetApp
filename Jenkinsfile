pipeline {
 agent any;
  stages {
    stage('Build') {
      steps {
        bat "dotnet run --project  C:/Users/Administrator/source/repos/WebApplication1/WebApplication1"
        bat "\"${MSBUILD}\" C:/Users/Administrator/source/repos/WebApplication1/WebApplication1.sln /p:Configuration=${env.CONFIG};Platform=${env.PLATFORM} /maxcpucount:%NUMBER_OF_PROCESSORS% /nodeReuse:false"
      }
    }
  }
 
 post {  
             
         success {  
           mail bcc: '', body: 'Hey, your job has ran successfully keep innovating.', cc: '', from: '', replyTo: '', subject: 'Job Succeeded from multi branch', to: 'amitsharma13317@gmail.com'  
         }  
         failure {  
             mail bcc: '', body: 'Hey, your job has failed. When you will up. Report to the office.', cc: '', from: '', replyTo: 'Job Failed from multi branch Need to Up', subject: '', to: 'amitsharma13317@gmail.com'
         }  
 }
}
