pipeline {
    agent {
        docker {
            image 'orestx/cv-android'
            label 'docker'
        }
    }
    stages {
        stage ('build') {
            steps {
                sh 'bash gradlew assembleRelease'
            }
        }
    }
}