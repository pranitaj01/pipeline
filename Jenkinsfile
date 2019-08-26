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
                    git 'https://github.com/pranitaj01/pipeline.git';
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
                sh 'echo deployed'
            }
        }
    }
}