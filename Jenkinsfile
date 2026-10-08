pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                bat 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
    }
    post {
    always {
        echo 'Pipeline execution completed'
    }

    success {
        echo 'Build passed'
    }

    failure {
        echo 'Build failed'
    }
}
}