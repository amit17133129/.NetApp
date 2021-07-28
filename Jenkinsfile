pipeline {
 agent any;
 environment {
    MSBUILD = "C:/Program Files (x86)/Microsoft Visual Studio/2019/Community/MSBuild/Current/Bin/MSBuild"
    CONFIG = 'Test'
    PLATFORM = 'AnyCPU'
    OutputPath = 'C:/Output/bin/'
     
  }
  stages {
    stage('Build') {
      steps {
    //    bat "dotnet run --project  C:/Users/Administrator/source/repos/WebApplication1/WebApplication1"
        bat "\"${MSBUILD}\" C:/Users/Administrator/source/repos/WebApplication4-7/WebApplication4-7 /p:Configuration=${env.CONFIG}   /p:OutputPath=${env.OutputPath}; Platform=${env.PLATFORM} /maxcpucount:%NUMBER_OF_PROCESSORS% /nodeReuse:false"
      }
    }
  }
   post {  
             
         success {  
           mail bcc: '', body: 'Hey, .Net Application run successfully.', cc: '', from: '', replyTo: '', subject: 'Job Succeeded', to: 'amitsharma13317@gmail.com'  
         }  
         failure {  
             mail bcc: '', body: 'Hey, .Net Application Failed', cc: '', from: '', replyTo: 'Job Failed', subject: '', to: 'amitsharma13317@gmail.com'
         }  
 }
}
