pipeline{
    agent any

    tools{
        maven 'maven'
    }

    stages{
        stage('hello')
        {
            steps{
                echo 'Hello DevOps!!'
            }
        }
        stage('pull src')
        {
            steps{
                git 'https://github.com/Aditya5576/JAR-TASK.git'
            }
        }
        stage('maven clean')
        {
            steps{
                sh 'mvn clean'
            }
        }
        stage('maven validate')
        {
            steps{
                sh 'mvn validate'
            }
        }
        stage('maven compile')
        {
            steps{
                sh 'mvn compile'
            }
        }
        stage('maven test')
        {
            steps{
                sh 'mvn test'
            }
        }
        stage('maven package')
        {
            steps{
                sh 'mvn package'
            }
        }
        stage('maven verify')
        {
            steps{
                sh 'mvn verify'
            }
        }
        stage('maven install')
        {
            steps{
                sh 'mvn install'
            }
        }
    }
    post{
        success{
            echo 'All tasks completed successfully.'
        }
        failure{
            echo 'One or more tasks failed.'
        }
    }
}
