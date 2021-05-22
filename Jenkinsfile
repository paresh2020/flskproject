pipeline {
    agent any
    stages
        {
            stage('Clone Reposirory')
            {
                steps
                {
                checkout scm
                }
            }
            stage('Build Image')
            {
                steps
                {
                sh 'sudo docker build . -t flaskr'
                }
            }
            stage('Run Image')
            {
                steps
                {
                sh 'sudo docker run -d -p 5000:5000 flaskr'
                }
            }
            stage('Test Image')
            {
                steps
                {
                sh 'echo "hi"'
                }
            }
        }
}
