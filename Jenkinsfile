pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Hello World'
                sh'''
                ls -la
                pwd
                ls -l
                cat > sample.txt
                rm sample.txt
                ls -a
                '''
            }
        }
        stage ('test'){
            steps{
                echo 'This is your first test case'
                test -f sample.txt
            }
        }
        
    }
}