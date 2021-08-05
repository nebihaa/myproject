node {
    stage('build') {
        git 'https://github.com/nebihaa/myproject.git'
        def dotapp = docker.build ' my-docker-app '
        dotapp.run()
        }
    }
}
