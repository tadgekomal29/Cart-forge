pipeline {
    agent any
    tools {
        nodejs 'npm'
    }
    environment {
        Name = "komal"
    }

    stages {
        stage('clone') {
            steps {
                echo 'Hello World'
                git branch: 'main', url: 'https://github.com/tadgekomal29/Cart-forge.git'
            }
        }
         stage('build') {
            steps {
                echo 'Hello World'
                sh 'npm i'
            }
        }
         stage('building the artifact') {
            steps {
                echo 'Hello World'
                sh 'npm run build'
            }
        }
        stage('s3 bucket deploy') {
            steps {
                echo 'Hello World'
                withCredentials([aws(accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: 'aws-cred', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY')]) {
    // some block
}
            }
     
    }
}
