pipeline {
    agent any
    
    parameters {
        booleanParam(name: 'Execute_Stage_2',
                     defaultValue: true,
                     description: 'Execute Stage 2')
    }
    
    stages {
        
        stage('Stage 1') {
            steps {
                echo 'Stage 1 done!' 
            }
        }
        
        stage('Stage 2') {
            steps {
                echo 'Stage 2 done!' 
            }
        }
        
        stage('Stage 3') {
            steps {
                echo 'Stage 3 done!' 
            }
        }
        
    }
}
