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
                  withAWS(region:'ca-central1',credentials:'s3-jenkins-project') {
                    sh 'echo "Uploading content with AWS creds"'
                     s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'liontechacademy-12')
                    
                     }
              }
 }
