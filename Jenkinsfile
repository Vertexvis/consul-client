pipeline {
    agent any
    stages {
        stage('Build and publish') {
            when { branch 'master' }
            steps {
                sh "docker run --rm -i -v ${env.WORKSPACE}:/app -v ${env.HOME}/.aws:/root/.aws -w /app maven:3.8.5-openjdk-17-slim ./build.sh"
            }
        }
    }
}
