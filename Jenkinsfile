pipeline {
        parameters {
            string (name: 'ANDROID_VERSION', defaultValue: '27')
            string (name: 'ANDROID_BUILD_TOOLS_VERSION', defaultValue: '27.0.2')
        }
    agent {
        docker {
            image 'orestx/cv-android:27-28.0.3'
            label 'docker'
        }
    }
    stages {
        stage ('build') {
            steps {
                sh '. $ENV'
                sh 'bash gradlew assembleRelease'
                sh 'ls -lh /usr/local/android-sdk/build-tools'
            }
        }
    }
}
