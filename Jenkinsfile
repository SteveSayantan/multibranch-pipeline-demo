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
               sh 'this only runs for PR' 
            }
        }   
    }
}
