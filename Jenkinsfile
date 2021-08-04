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
                 bat " dotnet build"
                 bat " dotnet test"
                   
                }
            }
        }   

    }
    
}
