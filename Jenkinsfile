/* Requires the Docker Pipeline plugin */
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building'
                sh 'pwd'
                sh 'ls -la'
                cmakeBuild buildType: 'Release', cleanBuild: true, installation: 'InSearchPath'
                sh 'make'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing main executable'
                sh './hello'
                echo 'Unit test'
                ctest 'InSearchPath'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
    }
}
