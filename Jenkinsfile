pipeline {
    agent any
    stages {
        stage('vcs') {
            steps{
              git url: 'https://github.com/CAESAR269/vm-tf.git'
                  branch: 'main'
           }
        }
        stage('terraform'){
            steps{
                sh 'terraform init'
                sh 'terraform validate'
                sh 'terraform plan'
                sh 'terraform apply --auto-approve'
            }
        }

    } 
}
