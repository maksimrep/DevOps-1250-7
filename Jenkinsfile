pipeline {
    agent { label 'Remote' }

    stages {
        stage('Clone the repo') {
            steps {
                echo 'Clone the repo'
                sh 'rm -fr DevOps-1250-7'
                sh 'git clone https://github.com/maksimrep/DevOps-1250-7.git'
            }
        }
        stage('Push repo to remote host') {
            steps {
                echo 'Connect to remote host'
                sh 'ssh -i ~/.ssh/id_rsa vagrant@192.168.100.101 sudo git -C /var/www/html pull'
            }
        }
    }
}
