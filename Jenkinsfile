pipeline {
    agent any

    stages {
        stage('docker build') {
            steps {
                script {
                    sh "docker build -f Dockerfile -t andres37/homerpage:v1-${BUILD_ID}"
                }
            }
        }
        stage('docker push') {
            steps {
                script {
                    sh "docker push andres37/homerpage:v1-${BUILD_ID}"
                }
            }
        }
    }
}
