pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /home/.m2:/home/.m2'
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
