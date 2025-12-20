pipeline {
    agent any
    stages {
        stage ("Build") {
            steps {
                sh 'docker build -t static1 .'
            }
        }
        
        stage ("Deploy") {
            steps {
                sh 'docker run -itd --name bus -p 8888:80 static1'
            }
        }
    }
}
