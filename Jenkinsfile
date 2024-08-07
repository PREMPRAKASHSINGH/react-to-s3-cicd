pipeline {
    agent any
    tools {
        nodejs 'node20'
    }

    stages {
        stage('clone repo') {
            steps {
                script{
                    git url: 'https://github.com/PREMPRAKASHSINGH/react-to-s3-cicd.git', branch: 'main'
                }
            }
        }
        
        stage('install dependencies') {
            steps {
                sh 'sudo npm install'
            }
        }
        
        stage('build app') {
            steps {
                sh 'sudo npm run build'
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
