pipeline {
  agent any
  stages {
    stage('build font') {
      steps {
        sh 'echo "use fontcustom to build font from svgs"'
        sh '''pwd
tar czf svgs.tar **/*.svg'''
      }
    }
    stage('Archive') {
      steps {
        archiveArtifacts(artifacts: 'svgs.tar', allowEmptyArchive: true, caseSensitive: true, onlyIfSuccessful: true)
      }
    }
  }
}