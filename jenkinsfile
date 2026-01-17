pipeline{
    agent any
    stages{
        stage("test"){
            steps{
                sh("uname")
                sh("uname -r")
            }
        }
        stage("dev"){
            steps{
                sh("free")
            }
        }
        
    }
}
