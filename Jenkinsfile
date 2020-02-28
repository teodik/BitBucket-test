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
                    bat('git remote add BitBucket https://bitbucket.org/teodik1979/github-test.git')
                    bat('git pull BitBucket test')
                    bat('git push -u GitHub test')
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