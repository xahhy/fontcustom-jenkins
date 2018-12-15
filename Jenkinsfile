pipeline {
  agent any
  stages {
    stage('build font') {
      steps {
        sh 'echo "use fontcustom to build font from svgs"'
      }
    }
    stage('Archive') {
      steps {
        archiveArtifacts(artifacts: 'fontcustom', allowEmptyArchive: true, caseSensitive: true, onlyIfSuccessful: true)
      }
    }
  }
}