pipeline {
    agent any
    
    parameters {
        booleanParam(name: 'Execute_Stage_2',
                     defaultValue: false,
                     description: 'Execute Stage 2')
    }
    
    stages {
        
        stage('Stage 1') {
            steps {
                echo "Parameter Execute_Stage_2: ${params.Execute_Stage_2}"
                echo "Branch name: ${params.BRANCH}"
                echo 'Stage 1 done!' 
            }
        }
        
        stage('Stage 2') {
            when {
                expression {
                    return params.Execute_Stage_2 || params.BRANCH != "origin/develop"
                }
            }
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
