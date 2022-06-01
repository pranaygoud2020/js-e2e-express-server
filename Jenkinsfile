pipeline {
    agent { label 'spc,123' }
   
    stages {
        stage('scm') {
            steps{
            git branch: 'main', url: 'https://github.com/Azure-Samples/js-e2e-express-server.git'
     }
        }
        stage('install npm and test') {
            steps {
        sh 'npm install'
        sh 'npm test'
        }
        }
        stage('build and start') {
            steps {
            sh 'npm run build'
            sh 'npm start &'
        }
        }
     
    }
}
