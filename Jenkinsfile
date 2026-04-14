pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/shreya20m/automationexercise.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package -DskipTests'
            }
        }

        //stage('Run Application') {
            //steps {
            //    sh 'java -jar target/automationexercise-1.0-SNAPSHOT.jar'
          //  }
        //}
    }

    post {
        success {
            echo '✅ Build and deployment successful!'
        }
        failure {
            echo '❌ Build failed!'
        }
    }
}
