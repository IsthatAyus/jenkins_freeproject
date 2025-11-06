pipeline{
    agent any 
    stages{
        stage('Build'){
            steps {
                echo 'Building..'
                sh 'python3 mypythonapp.py'
            }
        }

        stage('Test'){
            steps {
                echo 'Testing..'
                sh 'python3 mypythonapp.py | grep "devops"'
            }
        }
    }
}