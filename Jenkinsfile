pipeline {
    agent any 
    
    stages{
        stage('clean') {
            steps{
                cleanedWs()
                echo ' cleaned workspace for project ' 
            }
        }
        stage('checkout') {
            steps{
                checkout([ $class: 'GitSCM', branches: [[ name: '*/master' ]], userRemoteConfigs: [[ url:'https://github.com/nebihaa/myproject.git']]])
            }
        }
        stage('build') {
            
                def dotnetContainer = docker.build'dotnetImage'
                dotnetContainer.run()
            
        }
    }
}
