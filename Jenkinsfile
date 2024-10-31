pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -Dskiptests -Denforcer.skip=true clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
    }
}