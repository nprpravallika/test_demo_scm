pipeline {
    agent any
    parameters {
        string(name: 'PERSON', defaultValue: 'Pravallika', description: 'What is ur name?')
        string(name: 'PRODUCT', defaultValue: 'FW', description: 'enter the product name')
        string(name: 'VERSION', defaultValue: '2.2', description: 'enter the version number')
    }
    stages {
        stage('Example') {
            steps {
                echo "Hello ${params.PERSON}${params.PRODUCT}${params.VERSION}"
            }
        }
        stage('Example2') {
            steps {
                def filecontent = readJSON file: 'FW_2.2.json'
                filecontent.each { key, value ->
                    echo "Walked through key $key and value $value"
                }
            }
        }
    }
}
