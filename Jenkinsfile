pipeline {  
    agent any 
    
    stages {
        stage('Hello') {
            steps {
               sh 'echo Hello' 
            }
        }   
        stage('for the fix branch') {
            when {
               branch 'fix-*' 
            }
            steps {
               sh 'cat README.md' 
            }
        }   
        stage('for the PR') {
            when {
               branch 'PR-*' 
            }
            steps {
               sh 'echo this only runs for PR'
               sh 'echo change branch is $CHANGE_BRANCH'
               sh 'echo branch name is $BRANCH_NAME'
               sh 'echo GIT branch  is $GIT_BRANCH'
               sh 'echo git local branch name is $GIT_LOCAL_BRANCH'
                
            }
        }   
    }
}
