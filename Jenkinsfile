pipeline{
    agent any
    triggers{
        upstream(upstreamProjects:{'project1'})
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