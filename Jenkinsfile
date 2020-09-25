pipeline {
    agent any
    
    stages {
        stage('Test') {
            steps {
                dir('C:/Users/Usuario/Documents/Proyectos/SA/practica7'){
                    echo 'Testing..'
                        bat 'cd Cliente'
                        bat 'C:\\Users\\Usuario\\AppData\\Local\\Programs\\Python\\Python38-32\\Scripts\\coverage run main\\test.py'
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