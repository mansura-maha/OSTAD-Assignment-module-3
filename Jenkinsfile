pipeline { 
    agent any

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/mansura-maha/OSTAD-Assignment-module-3.git'
            }
        }

        stage('Install') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm run check'
            }
        }
    }

    post {
        success {
            echo '✅ Build was successful!'
        }
        failure {
            echo '❌ Build failed. Check the logs.'
        }
    }
}

