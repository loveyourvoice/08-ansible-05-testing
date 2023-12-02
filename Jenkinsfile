pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
                echo 'Hello World'
                git credentialsId: '22bbb3e0-906f-4593-8ab2-daea54d2e174', 
                url: 'https://github.com/loveyourvoice/08-ansible-05-testing.git',
                branch: 'master'
            }
        }
        stage('test') {
            steps {
                echo 'Run molecule test'
                sh 'cd roles/vector-role && molecule test'
            }
        }
    }
}
