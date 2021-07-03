pipeline {
    agent any
      stages {
          stage('configuring dotnet repo and installing dotnet'){
                steps {
                  //  sh 'sudo rpm -Uvh https://packages.microsoft.com/config/centos/7/packages-microsoft-prod.rpm' 
                    sh 'sudo yum install dotnet-sdk-5.0 -y'
                    sh 'sudo yum install aspnetcore-runtime-5.0 -y'

   
                }
        }
         stage('Creating new console and running dotnet app'){ 
               steps {
                    sh 'sudo dotnet new console'
                    sh 'sudo dotnet run'
             }
        }
    }
}
