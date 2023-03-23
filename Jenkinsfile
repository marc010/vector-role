pipeline {
    agent any

    stages {
        stage('Get repo') {
            steps {
                git branch: 'main', url: 'https://github.com/marc010/vector-role.git'
            }
        }        
        stage('Run molecule test') {
            steps {
                sh 'molecule test -s ubuntu_latest'
            }
        }
    }
}