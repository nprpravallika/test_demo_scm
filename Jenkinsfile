pipeline {
    agent any
    parameters {
        string(name: 'PERSON', defaultValue: 'Pravallika', description: 'What is ur name?')
    }
    stages {
        stage('Example') {
            steps {
                echo 'Hello ${params.PERSON}'
            }
        }
    }
}
