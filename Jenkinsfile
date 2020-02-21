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
                script{
                    bat('git remote add github https://github.com/teodik/BitBucket.git')
                    bat('git remote -v')
                    bat('git branch')
                }
            }
        }
    }
}