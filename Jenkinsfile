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
                echo "Parameter Execute_Stage_2: ${params.Execute_Stage_2}"
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
