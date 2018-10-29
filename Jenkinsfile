pipeline {
    agent {
        docker {
            image 'orestx/cv-android:27-28.0.3'
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