pipeline{
    agent any

    tools {
         maven 'maven-1:3.6.3-14.el9.noarch'
         jdk 'java-11-openjdk-1:11.0.19.0.7-1.el9_1.x86_64'
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
