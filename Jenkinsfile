@Library('jyothihome-lbs') _
pipeline{
    agent any
    tools{
        maven 'maven3'
    }
    stages{
        stage("Maven Build"){
            steps{
                sh 'mvn clean package'
            }
        }
        stage("Deploy to Tomcat Dev"){
            steps{
                tomcatDeploy('tomcat-dev','ec2-user','172.31.18.24')      
            }
        }
    }
}

