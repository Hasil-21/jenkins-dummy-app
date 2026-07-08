pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checkout is handled automatically by Jenkins when using a Pipeline job pointed at SCM'
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Build stage: nothing to compile in a shell script, but this is where you would run npm install, dotnet build, etc."'
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
