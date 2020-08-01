pipeline {
     agent any
     stages {
         stage('Upload to AWS') {
             steps {
                 withAWS(region:'us-west-2',credentials:'blueocean') {
                     s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:'index.html', bucket:'chrisp-udacity-project3')
                 }
             }
         }
    }
}
