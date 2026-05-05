pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building application...'
                sh '''
                echo "Hello DevOps" > sample.txt
                ls -la
                pwd
                '''
            }
        }

        stage('Test') {
            steps {
                echo 'Running test case...'
                sh '''
                if [ -f sample.txt ]; then
                    echo "Test Passed: File exists"
                else
                    echo "Test Failed: File not found"
                    exit 1
                fi
                '''
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution completed'
        }
        success {
            echo 'Build Success ✅'
        }
        failure {
            echo 'Build Failed ❌'
        }
    }
}