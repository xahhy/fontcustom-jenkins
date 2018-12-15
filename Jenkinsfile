pipeline {
  agent any
  stages {
    stage('build font') {
      steps {
        sh 'echo "use fontcustom to build font from svgs"'
        sh('build.sh')
      }
    }
    stage('Archive') {
      steps {
        archiveArtifacts(artifacts: 'svgs.tar', allowEmptyArchive: true, caseSensitive: true, onlyIfSuccessful: true)
      }
    }
  }
}