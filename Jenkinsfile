pipeline {
    agent any

    stages {
        stage('docker build') {
            steps {
                script {
                    sh "docker build -f 02-primer-pipeline/Dockerfile -t andres37/homerpage:v1-${BUILD_ID} 02-primer-pipeline"
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
