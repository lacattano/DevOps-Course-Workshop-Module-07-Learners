pipeline {
    agent none
    stages {
        stage('Build') {
        agent {docker {image "mcr.microsoft.com/dotnet/sdk:6.0"} }   
            steps {
                checkout scm
               sh "dotnet build"
               sh "dotnet test"
            }
        environment {DOTNET_CLI_HOME = "/tmp/dotnet_cli_home"}
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}