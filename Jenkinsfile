pipeline{
    agent any
    stages{
        stage("test"){
            steps{
                sh("uname")
                sh("uname -r")
                sh("git diff HEAD~1 HEAD")
                sh("git diff --name-only HEAD~1 HEAD")
                script{
                    def filechanges=sh(script: 'git diff --name-only HEAD~1 HEAD',returnStdout: True)
                    echo "Changed filename is ${filechanges}"
                }
                   
            }
        }
        stage("dev"){
            steps{
                sh("free")
            }
        }
        
    }
}
