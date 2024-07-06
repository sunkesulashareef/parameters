pipeline {
    agent {
        label 'prod'
    }
    environment {
        app_name='sailor'
        version='1.0'
    }
    parameters {
        string(name:'ipaddress',defaultValue:'0.0.0.0')
        choice choices:['DEV','PROD','TEST','UAT'], name: 'ENV'
        text name: 'descr'
        booleanParam name: 'DEPLOY', defaultValue: true, description: 'deploy the project'
    }
    stages {
        stage ('build') {
            steps {
                echo "${params.ipaddress}"
                echo "${params.ENV}"
                echo "${params.DEPLOY}"
            }
        }
    }
}