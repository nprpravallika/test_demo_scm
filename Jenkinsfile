pipeline {
    agent any
    parameters {
        string(name: 'PERSON', defaultValue: 'Pravallika', description: 'What is ur name?')
    }
    stages {
        stage('Example') {
            steps {
                echo "Hello ${params.PERSON}_${params.VERSION}"
            }
        }
        stage('Example2') {
            steps {
                def filecontent = readJSON file: "${env.WORKSPACE}\\${params.PRODUCT}_${params.VERSION}.json"
                filecontent.each { key, value ->
                    echo "Walked through key $key and value $value"
                }
            }
        }
    }
}
