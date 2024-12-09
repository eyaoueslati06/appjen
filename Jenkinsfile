pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], 
                          userRemoteConfigs: [[url: 'https://github.com/eyaoueslati06/appjen.git', 
                          credentialsId: 'github-credentials']]])
            }
        }
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Java Version') {
            steps {
                bat 'cmd /c java -version'
            }
        }
    }
}
