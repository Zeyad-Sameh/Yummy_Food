pipeline{
    agent any

    stages{
        stage('build'){
            steps{
                script{
                    echo "build in progress"
                }
            }
        }
        stage('test'){
            steps{
                script{
                    echo "test in progress"
                }
            }
        }
    }
    post {
  success {
    slackSend channel: 'jenkins-ci', message: 'Build Sucess - ${env.JOB_NAME} ${env.BUILD_NUMBER} (<${env.BUILD_URL}|Open>)', teamDomain: 'teamelzoz', tokenCredentialId: 'notification'
  }
  failure {
    slackSend channel: 'jenkins-ci', message: 'Build fail- ${env.JOB_NAME} ${env.BUILD_NUMBER} (<${env.BUILD_URL}|Open>)', teamDomain: 'teamelzoz', tokenCredentialId: 'notification'
  }
}
}