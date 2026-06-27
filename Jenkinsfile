pipeline {
    agent any

    environment {
        DOTNET_ROLL_FORWARD = 'Major'
    }

    stages {
        stage('Restore') {
            steps {
                bat 'dotnet restore'
            }
        }
        stage('Build') {
            steps {
                bat 'dotnet build --configuration Release --no-restore'
            }
        }
        stage('Test') {
            steps {
                bat 'dotnet test --no-build --configuration Release'
            }
        }
    }
}