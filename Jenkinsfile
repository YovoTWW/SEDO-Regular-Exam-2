pipeline {
    agent any

    stages {

        stage('Checkout the Repository') {
            steps {
                checkout scm
                }
        }

        stage('Restore the project') {
            steps {          
                bat 'dotnet restore'
            }
        }          
        
        stage('Build the project') {
            steps {            
                    bat 'dotnet build --no-restore'
            }
        }            

        stage('Run test') {
            steps {            
                    bat 'dotnet test --no-build --verbosity normal'           
                    }
            }
    }
}