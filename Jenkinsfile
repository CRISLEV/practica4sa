pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                cd Cliente
                coverage run main/test.py
                coverage report
                coverage xml
                rename coverage.xml coverage-client.xml
                cd ..
                move Cliente/coverage-client.xml Reports
                cd esb
                coverage run main/test.py
                coverage report
                coverage xml
                rename coverage.xml coverage-esb.xml
                cd ..
                move esb/coverage-esb.xml Reports
                cd Repartidor
                coverage run main/test.py
                coverage report
                coverage xml
                rename coverage.xml coverage-repartidor.xml
                cd ..
                move Repartidor/coverage-repartidor.xml Reports
                cd Restaurante
                coverage run main/test.py
                coverage report
                coverage xml
                rename coverage.xml coverage-restaurante.xml
                cd ..
                move Restaurante/coverage-restaurante.xml Reports
            }
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