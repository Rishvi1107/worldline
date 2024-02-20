pipeline {
    agent { 
        node {
            label 'my_pc'
            }
      }
    triggers {
        pollSCM '* * * * *'
    }
     stages {
        stage('Build') {
            steps {
                echo "Building.."
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                bat '''
                C:/Users/rishv/AppData/Local/Programs/Python/Python311/python.exe 
                python hello.py
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo "Delivery.."
            }
        }
    }
}
