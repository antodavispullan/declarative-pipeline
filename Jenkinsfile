pipeline{
    agent any
    triggers{
        pollSCM("* * * * *")
    }
    stages{
        stage('compile'){
            steps{
                sh 'echo Hello World'
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
    }
}