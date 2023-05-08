pipeline{
    agent any

    tools {
         maven 'maven'
         jdk 'jdk'
    }

    stages{
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/santhosh-git-23/hello-world-maven.git']]])
            }
        }
        stage('build'){
            steps{
               bat 'mvn package'
            }
        }
        
    }
}
