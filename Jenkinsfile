pipeline {
     agent any
     stages {
         stage('Upload to S3') {
             steps {
                 withAWS(region:'us-east-2',credentials:'aws-static') {
                 sh 'echo "Uploading content with AWS creds"'
                     s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'project-3-course')
                 }
             }
         }
     }
}
