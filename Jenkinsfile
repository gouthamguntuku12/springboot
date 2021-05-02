
pipeline {
    agent any
    environment {
        PATH = "/opt/apache-maven-3.8.1/bin/:$PATH"
    }

    stages {
        stage('fetch code from github') {
            steps {
                git 'https://github.com/gouthamguntuku12/springboot.git'
            }
        }
        stage('build a package') {
            steps {
                sh 'mvn clean validate compile test package install'
            }
        }
    }
}
