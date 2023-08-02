pipeline {
  agent any
  stages {
    stage('build-the-app-bycode') {
      steps {
        echo 'this is the build job'
        sh 'npm install'
      }
    }

    stage('test-the-app-bycode') {
      steps {
        echo 'this is the test job'
        sh 'npm test'
      }
    }

    stage('pacakage-the-app-bycode') {
      steps {
        echo 'this is the package job'
        sh 'npm run package'
      }
    }

    stage('Archive') {
      steps {
        archiveArtifacts '**/distirbution/*.zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'this pipeline has completed...by Rajneesh'
    }

  }
}