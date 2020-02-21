pipeline{
    agent any
    stages{
        stage('print a message'){
            steps{
                echo "webhook works let see"
            }
        }
        stage('Git status'){
            steps{
                sh 'git remote -v'
            }
        }
    }
}