pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'chmod +x src/hello.sh'
                sh './src/hello.sh'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing the project...'
                sh 'test -f src/hello.sh'
                sh 'grep -q "Hello from my Jenkins CI/CD project!" src/hello.sh'
                echo 'All tests passed!'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment demo completed successfully.'
            }
        }
    }
}
