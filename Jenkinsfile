node('built-in') {
  stage('Build') {
    git 'https://github.com/pratik-shah2611/trainingMaterial.git'
    
    withCredentials([usernamePassword(credentialsId: 'artifactory-creds', passwordVariable: 'apass', usernameVariable: 'auser')]) {
      sh '''
        hostname
        echo "Building my project and pushing artifacts to artifactory with credentials $auser : $apass "
        pwd
        ls -ltra
        '''
    }
  }
}

node('vemaztechtrg202') {
  stage('Deploy') {
    sh '''
      hostname
      echo "Deploying application on QA"
      pwd
      ls -ltr
      '''
  }
  
  stage('QATesting') {
    sh'''
      hostname
      echo "This job performs QA Testing"
      '''
  }
}
