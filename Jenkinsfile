pipeline{
    agent:any
    triggers{
        cron("* * * * *")
    }
    stages{
        stage('compile'){
            steps{
                sh 'echo Hello World'
            }
        }
    }
    post:{
         always{
             sh 'echo build completed'
         }
         changed{
             sh 'echo  build changed'
         }
    }
}