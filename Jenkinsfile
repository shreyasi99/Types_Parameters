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
                                name: 'PARAMETER_01',
                                defaultValue:'ONE'
                            ),
                            booleanParam(
                                defaultValue: true, 
                                
                                name: 'BOOLEAN'
                            ),
