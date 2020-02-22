pipeline{
    agent any
    stages{
        stage('clean up working directory'){
            steps{
                cleanWs()
                bat('dir')
            }
        }
        stage('Synchrinizing BitBucket with GitHub'){
            steps{
                script{
                    bat('md myrepository')
                    bat('cd myrepository')
                    bat('git init')
                    bat('git remote add GitHub https://github.com/teodik/BitBucket.git')
                    bat('git remote add BitBucket https://bitbucket.org/teodik1979/github.git')
                    bat('git pull BitBucket master')
                    bat('git push -u GitHub master')
                }
            }
        }
    }
    post{
        always{
            cleanWs()
        }
    }
}