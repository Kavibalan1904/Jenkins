    pipeline {
        agent any 
        stages {
            stage('git clone') {
                steps {
                git credentialsId: 'c8103480-c032-4167-a9b2-5ae674340d48', url: 'https://github.com/Kavibalan1904/Jenkins.git'
                }
            }
            stage('maven build') {
                steps {
                    sh 'mvn clean package'
                }
            }
            stage('java test') {
                steps {
                sh 'java -jar target/AWS-1.0-SNAPSHOT.jar'
                }
            }
        }
    }
