pipeline {
    agent any
    stages{
        stage(" Clean Up") {
            steps{
                deleteDir()
            }

        }
        stage("build") {
            steps {
                dir ("myproject") {
                 sh " dotnet build " ConsolApp1.csproj" "
                 
                   
                }
            }
        }   

    }
    
}
