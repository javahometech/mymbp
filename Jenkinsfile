pipeline{
    options {
        buildDiscarder logRotator(daysToKeepStr: '10', numToKeepStr: '5')
    }
    agent any 
    stages{
        stage("SCM"){
            steps{
               echo "job ran..."
            }
        }
    }
}
