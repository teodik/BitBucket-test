pipeline{
    agent any
    stages{
        stage('print a message'){
            steps{
                cleanWs()
                echo "webhook works let see"
            }
        }
        stage('Git status'){
            steps{
                script{
                    bat('md myrepository')
                    bat('cd myrepository')
                    bat('git init')
                    bat('git remote add GitHub https://github.com/teodik/BitBucket.git')
                    bat('git remote add BitBucket https://bitbucket.org/teodik1979/github.git')
                    bat('git remote -v')
                    bat('git pull BitBucket master')
                    bat('git branch -v')
                    bat('git branch --track BB BitBucket/master')
                    bat('git checkout BB')
                    bat('git checkout -b GH')
                    bat('dir')
                    bat('git branch -vvv')
                    bat('git push -u GitHub master')
                }
            }
        }
    }
}