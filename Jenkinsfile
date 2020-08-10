pipeline {
    agent any
    
    parameters {
        booleanParam(name: 'Execute_Stage_2',
                     defaultValue: false,
                     description: 'Execute Stage 2')
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    
    stages {
        
        stage('Stage 1') {
            steps {
                echo "Parameter Execute_Stage_2: ${params.Execute_Stage_2}"
                echo 'Stage 1 done!' 
            }
        }
        
        stage('Stage 2') {
            when {
                expression {
                    return params.Execute_Stage_2
                }
                not {
                    allOf {
                        branch 'develop'
                    }
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
