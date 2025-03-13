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
               sh 'echo $CHANGE_BRANCH'
               sh 'echo $BRANCH_NAME'
                
            }
        }   
    }
}
