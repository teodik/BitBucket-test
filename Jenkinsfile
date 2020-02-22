pipeline{
    agent any
    stages{
        stage('print a message'){
            steps{
                cleanWs()
                echo "webhook works let see"
                script{
                    scm_map = checkout scm
                }
            }
        }
        stage('Git status'){
            steps{
                script{
                    bat('dir')
                    bat('git remote -v')
                    bat('git remote add github https://github.com/teodik/BitBucket.git')
                    bat('git remote -v')
                    bat('git pull origin master')
                    bat('git branch --track bb origin/master')
                    bat('git checkout bb')
                    bat('git checkout -b gb')
                    bat('git branch -vv')
                    bat('dir')
                    //bat('git push github master')
                }
            }
        }
    }
}