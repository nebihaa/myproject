pipeline {
    agent any 
    
    stages{
        stage('clean') {
            steps{
                cleanWs()
                echo ' cleaned workspace for project ' 
            }
        }
        stage('checkout') {
            steps{
                checkout([ $class: 'GitSCM', branches: [[ name: '*/master' ]], userRemoteConfigs: [[ url:'https://github.com/nebihaa/myproject.git']]])
            }
        }
        stage('build') {
         steps{
            script{
                def dotnetContainer = docker.build'dotnetimage'
                dotnetContainer.run()
              }
            }
        }
    }
}
