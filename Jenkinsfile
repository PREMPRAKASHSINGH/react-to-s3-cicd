pipeline {
    agent any

    stages {
        stage('clone repo') {
            steps {
                script{
                    git 'git@github.com:PREMPRAKASHSINGH/react-to-s3-cicd.git'
                }
            }
        }
        
        stage('install dependencies') {
            steps {
                sh 'npm install'
            }
        }
        
        stage('build app') {
            steps {
                sh 'npm run build'
            }
        }
        
        // stage('build app') {
        //     echo 'deploying...'
        //     steps {
        //         // sh 'npm run build'
        //     }
        // }
    }
}
