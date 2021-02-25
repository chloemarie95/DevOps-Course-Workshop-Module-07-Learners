pipeline {
    agent any

    stages {
        stage('Build and Test C# code'){
            agent{
                docker{
                    image 'mcr.microsoft.com/dotnet/sdk:5.0'
                }
            } 
            environment {
                DOTNET_CLI_HOME = "/tmp/DOTNET_CLI_HOME"
            }
            steps {
                sh 'dotnet build'
                sh 'dotnet test'
            }
        }
        stage('Build and Test Typescript code') {
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