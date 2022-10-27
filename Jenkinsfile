pipeline {
    agent any

    stages {      
        stage('apache2 instaland build') {
            steps{
                sh 'sudo apt install apache2 -y'
                sh 'sudo rm -rf /var/www/html/*'
                sh 'sudo cp -r /var/lib/jenkins/workspace/coronapp/* /var/www/html/'
            }
        }
    }
}
