pipeline{
    agent any

    tools {
         maven 'maven 3.9.1'
         jdk 'jdk'
    }

    stages{
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'https://github.com/santhosh-git-23/hello-world-maven.git']]])
            }
        }
        stage('build'){
            steps{
               bat 'mvn package'
            }
        }
    }
}
