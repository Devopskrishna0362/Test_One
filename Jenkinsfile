pipeline {
    agent any

    stages {
        stage('Hello') {
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
                test -f sample.txt
            }
        }
        
    }
}