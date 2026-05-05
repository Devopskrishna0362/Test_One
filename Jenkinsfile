pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                sh'''
                ls -la
                pwd
                touch account.txt
                '''
            }
        }
    }
}