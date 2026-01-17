pipeline{
    agent any
    stages{
        stage("test"){
            steps{
                sh("uname")
                sh("uname -r")
                sh("git diff HEAD~1 HEAD")
                sh("git diff --name-only HEAD~1 HEAD)
                   
            }
        }
        stage("dev"){
            steps{
                sh("free")
            }
        }
        
    }
}
