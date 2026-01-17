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
                    def filechanges=sh(script: 'git diff --name-only HEAD~1 HEAD',returnStdout: true)
                    echo "Changed filename is ${filechanges}"
                    echo "Below are content of file"
                    sh ("cat ~/workspace/Testpipline/${filechanges}")
                    echo "${BUILD_NUMBER}  ${WORKSPACE}"
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
