pipeline {
    agent { label 'agent-1' }

    stages {
        stage('Checkout') {
            steps {
                echo 'Checkout is handled automatically by Jenkins when using a Pipeline job pointed at SCM'
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Build stage running on: $(hostname)"'
            }
        }

        stage('Test') {
            steps {
                sh 'echo "Test stage: this is where unit tests would run"'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                    chmod +x app.sh
                    ./app.sh
                '''
            }
        }
    }
}
