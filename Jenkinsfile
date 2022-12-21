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
                     s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'components.html', bucket:'liontechacademy-12')
                     s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'main.bc58148c.js.gz', bucket:'liontechacademy-12')
                     s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'assets', bucket:'liontechacademy-12')
                     s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'sample', bucket:'liontechacademy-12')
                     s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'main.bc58148c.js', bucket:'liontechacademy-12')
                     s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'main.bc58148c.map', bucket:'liontechacademy-12')
                     s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'main.d8e0d294.css', bucket:'liontechacademy-12')
                     s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'main.d8e0d294.css.gz', bucket:'liontechacademy-12')
                     }
              }
         }
}
}
