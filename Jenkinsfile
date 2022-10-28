pipeline {
    agent any
         stages{
        stage ('Bulding docker docker image') {
            steps {
                echo "build docker image"
                sh 'docker build --no-cache -t demo .'
            }
        }
        
}
  
}  
