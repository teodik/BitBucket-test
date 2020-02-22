pipeline{
    agent any
    stages{
        stage('print a message'){
            steps{
                cleanWs()
                echo "webhook works let see"
                /*script{
                    scm_map = checkout scm
                }*/
            }
        }
        stage('Git status'){
            steps{
                script{
                    /*bat('dir')
                    bat('git remote -v')
                    bat('git remote add github https://github.com/teodik/BitBucket.git')
                    bat('git remote -vvv')
                    bat('git pull origin master')
                    bat('git branch --track bb origin/master')
                    //bat('git branch --track gb github/master')
                    bat('git checkout bb')
                    bat('dir')
                    //bat('git checkout gb')
                    bat('git branch -vv')
                    //bat('dir')
                    //bat('git push github master')*/
                    bat('md myrepository')
                    bat('cd myrepository')
                    bat('git init')
                    bat('git remote add GitHub https://github.com/teodik/BitBucket.git')
                    bat('git remote add BitBucket https://bitbucket.org/teodik1979/github.git')
                    bat('git remote -v')
                    bat('git pull BitBucket master')
                    bat('git branch --track BB BitBucket/master')
                    bat('git checkout BB')
                    bat('git checkout -b GH')
                    bat('dir')
                    bat('git branch -vvv')
                }
            }
        }
    }
}