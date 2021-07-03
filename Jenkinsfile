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
}
