pipeline {
    agent any
    stages{
        stage(" Clean Up") {
            steps{
                deleteDir()
            }

        }
        stage("clone repo") {
            steps {
                bat " git clone https://github.com/nebihaa/myproject.git"
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