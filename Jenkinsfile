pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Hello World"'
        sh '''
            echo  "Multi line shell steps works too"
            ls -lah
        ''' 
      }
    }
  }
}
 stage('Upload to AWS') {
              steps {
                  withAWS(region:'us-west-1',credentials:'Jenkins-cred') {
                  sh 'echo "Uploading content with AWS creds"'

