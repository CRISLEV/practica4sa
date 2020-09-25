pipeline {
    agent any
    
    stages {
        stage('Test') {
            steps {
                dir('C:/Users/Usuario/Documents/Proyectos/SA/practica7'){
                    echo 'Testing..'
                    bat 'cd Cliente'
                    bat 'C:\\Users\\Usuario\\AppData\\Local\\Programs\\Python\\Python38-32\\Scripts\\coverage run main\\test.py'
                    bat 'C:\\Users\\Usuario\\AppData\\Local\\Programs\\Python\\Python38-32\\Scripts\\coverage report'
                    bat 'C:\\Users\\Usuario\\AppData\\Local\\Programs\\Python\\Python38-32\\Scripts\\coverage xml'
                    bat 'RENAME coverage.xml coverage-client.xml'
                    bat 'cd ..'
                    bat 'MOVE Cliente\\coverage-client.xml Reports'
                    bat 'cd esb'
                    bat 'C:\\Users\\Usuario\\AppData\\Local\\Programs\\Python\\Python38-32\\Scripts\\coverage run main\\test.py'
                    bat 'C:\\Users\\Usuario\\AppData\\Local\\Programs\\Python\\Python38-32\\Scripts\\coverage report'
                    bat 'C:\\Users\\Usuario\\AppData\\Local\\Programs\\Python\\Python38-32\\Scripts\\coverage xml'
                    bat 'RENAME coverage.xml coverage-esb.xml'
                    bat 'cd ..'
                    bat 'MOVE esb\\coverage-esb.xml Reports'
                    bat 'cd Repartidor'
                    bat 'C:\\Users\\Usuario\\AppData\\Local\\Programs\\Python\\Python38-32\\Scripts\\coverage run main\\test.py'
                    bat 'C:\\Users\\Usuario\\AppData\\Local\\Programs\\Python\\Python38-32\\Scripts\\coverage report'
                    bat 'C:\\Users\\Usuario\\AppData\\Local\\Programs\\Python\\Python38-32\\Scripts\\coverage xml'
                    bat 'RENAME coverage.xml coverage-repartidor.xml'
                    bat 'cd ..'
                    bat 'MOVE Repartidor\\coverage-repartidor.xml Reports'
                    bat 'cd Restaurante'
                    bat 'C:\\Users\\Usuario\\AppData\\Local\\Programs\\Python\\Python38-32\\Scripts\\coverage run main\\test.py'
                    bat 'C:\\Users\\Usuario\\AppData\\Local\\Programs\\Python\\Python38-32\\Scripts\\coverage report'
                    bat 'C:\\Users\\Usuario\\AppData\\Local\\Programs\\Python\\Python38-32\\Scripts\\coverage xml'
                    bat 'RENAME coverage.xml coverage-restaurante.xml'
                    bat 'cd ..'
                    bat 'MOVE Restaurante\\coverage-restaurante.xml Reports'
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