pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -Dskiptests -Denforcer.skip=true clean package'
            }
        }
    }
}