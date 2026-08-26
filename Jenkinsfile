pipeline{
    agent any maven

    stages{
        stage('git') {
            steps {
                git credentialsId: 'c8103480-c032-4167-a9b2-5ae674340d48', url: 'https://github.com/Kavibalan1904/Jenkins.git'
                echo 
            }

    stage('version')  
        steps {
            sh 'mvn versions:set -DnewVersion=1.0.1'  
        
        }

    stage('build')
        steps 
{
            sh 'mvn clean package'
            echo 'Build completed successfully.'
        }
    stage('deploy')
        steps {
            sh 'cp '/AWS/target/classes/App.class' 
           echo 'Deployment completed successfully.'
        }
    }
}
}
