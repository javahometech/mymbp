pipeline{
    agent any
    tools {
        maven 'maven3'
    } 
    stages{
        stage("Maven Build"){
            when{
                branch 'develop'
            }
            steps{
               sh "mvn clean package"
            }
        }
        stage("Sonar Analysis"){
            when{
                branch 'develop'
            }
            steps{
               echo "doing sonar scaning..."
            }
        }
        stage("Upload to Nexus"){
            when{
                branch 'develop'
            }
            steps{
               echo "upload to nexus"
            }
        }
        stage("deploy to dev"){
            when{
                branch 'develop'
            }
            steps{
               echo "deploy to dev"
            }
        }
        stage("deploy to uat"){
            when{
                branch 'uat'
            }
            steps{
               echo "deploy to uat"
            }
        }
        stage("deploy to prod"){
            when{
                branch 'master'
            }
            steps{
               echo "deploy to master"
            }
        }

    }
}
