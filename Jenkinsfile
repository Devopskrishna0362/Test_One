pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Hello World'
                sh '''
                echo "sample data" > sample.txt
                ls -la
                pwd
                #rm sample.txt
                '''
            }
        }

        stage('Test') {
            steps {
                echo 'This is your first test case'
                sh '''
                if [ -f sample.txt ]; then
                    echo "Test Passed"
                else
                    echo "Test Failed"
                    exit 1
                fi
                '''
            }
    }
      stage('Prod'){
         steps{
             echo 'this is your test state'
             }
         }
       }
    post {
        always {
            echo 'Pipeline completed'
        }
        success {
            echo 'Build Successful ✅'
        }
        failure {
            echo 'Build Failed ❌'
        }
    }
}
