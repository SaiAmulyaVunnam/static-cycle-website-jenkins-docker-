pipeline {
    agent any
    stages {
        stage ("Build") {
            steps {
                sh 'docker build -t staticbuild .'
            }
        }
        stage ("Deploy") {
            steps {
                sh 'docker run -itd --name static -p 4455:80 staicbuild'
            }
        }
    }
}
