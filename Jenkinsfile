pipeline {
      agent any
      stages {
            stage('Upload to AWS.') {
                steps {
                    withAWS(region:'us-west-2',credentials:"Aws-Static") {
                        s3Upload(file:'index.html', bucket:'udacity-adelm', path:'index.html')
                    sh 'echo "Hello World"'
                    sh '''
                        echo "Multiline shell steps works too"
                        ls -lah
                    '''
                  }

            }
        
      }
}
