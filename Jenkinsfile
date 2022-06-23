pipeline {
    agent any

    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
        stage('Test') {
           steps {
               sh 'mvn test'
           }
           post {
               always {
                   junit 'target/surefire-reports/*.xml'
               }
            }
        }
        stage('build test')
           steps {
               sh 'mvn compile'
           }
           steps {
               sh 'mvn clean'
           }
    }
}

