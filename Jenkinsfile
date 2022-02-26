pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
          stage('Build Docker image') {
        steps {
            echo 'Running build Docker image'
            sh 'docker build -t cloudtesttt/docker-image-guru:v1.0.0 .'

        }
    }
    }
}
