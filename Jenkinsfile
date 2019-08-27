pipeline{
    agent any;
    stages{
        stage('Cleanup'){
            steps{
                cleanWs();
            }
        }
        stage('Checkout SCM'){
                steps{
                    checkout scm;
                }
        }
        stage('Build'){
            steps{
                sh 'chmod +x app.sh'
                sh 'echo Building'
            }
        }
        stage('test'){
            steps{
                sh 'sh app.sh'
                sh 'echo Testing'
            }
        }
        stage('deploy'){
            steps{
                sh 'echo deployment of August'
            }
        }
    }
}