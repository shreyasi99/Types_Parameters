pipeline {
    agent any
    stages {
        stage('Setup parameters') {
            steps {
                script { 
                    properties([
                        parameters([
                            choice(
                                choices: ['ONE', 'TWO'], 
                                name: 'PARAMETER_01'
                            ),
                            booleanParam(
                                defaultValue: true, 
                                
                                name: 'BOOLEAN'
                            ),
                            text(
                                defaultValue: '''
                                this is a multi-line 
                                string parameter example
                                ''', 
                                 name: 'MULTI-LINE-STRING'
                            ),
                            string(
                                defaultValue: 'scriptcrunch', 
                                name: 'STRING-PARAMETER', 
                                
                            )
                        ])
                    ])
                     stages {
        stage('Example') {
            steps {
                echo "PARAMETER_01: ${params.PARAMETER_01}"
                sh "echo PARAMETER_01: ${params.PARAMETER_01}"
                sh 'echo PARAMETER_01: $PARAMETER_01'
            }
        }
    }
                }
            }
        }
    }   
}
