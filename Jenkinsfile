pipeline {
    agent any
    
    stages {
        stage('Test') {
            steps {
                dir('C:/Users/Usuario/Documents/Proyectos/SA/practica7'){
                    echo 'Testing..'
                    bat 'build.bat'
                }
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}