pipeline{
    agent any
    triggers{
        pollSCM("* * * * *")
        upstream(upstreamProjects: 'project1', threshold: hudson.model.Result.SUCCESS)       
    }
    stages{
        stage('compile'){
            steps{
                sh 'echo Hello World'
                exit 1
            }
        }
        stage('Test'){
            steps{
                sh 'echo Testing...'               
            }
        }
    }
    post {
         always{
             sh 'echo build completed'
         }
         changed{
             sh 'echo  build changed'
         }
         fixed{
             sh 'echo  build fixed'
         }
         failure{
             sh 'echo  build failed'
         }        
         success{
             sh 'echo  build success'
         } 
    }
}