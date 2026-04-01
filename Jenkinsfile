pipeline {

    agent any
 
    stages {

        stage('Checkout') {

            steps {

                echo 'Checking out code...'

                checkout scm

            }

        }
 
        stage('Build') {

            steps {

                echo 'Build stage (Python check)...'

                sh 'python3 --version'

            }

        }
 
        stage('Test') {

            steps {

                echo 'Running tests...'

                sh '''

                python3 - <<EOF

import calculator
 
assert calculator.add(2,3) == 5

assert calculator.subtract(5,3) == 2

assert calculator.multiply(2,3) == 6

assert calculator.divide(6,3) == 2

print("All tests passed")

EOF

                '''

            }

        }
 
        stage('Deploy') {

            steps {

                echo 'Deploy stage (dummy)'

            }

        }

    }

}
 
