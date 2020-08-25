pipeline {
    agent any

    stages {
        stage('Checkout From Repository') {
            steps {
                git credentialsId: 'Github_Creds', url: 'https://github.com/kmahesh0124/Jenkins-Pipelines-Demo.git'
            }
        }
        stage('Maven Install') {
            steps {
                sh label: '', script: 'mvn install'
            }
        }
        stage('Cleanup Workspace') {
            steps {
                cleanWs()
            }
        }
    }
}
