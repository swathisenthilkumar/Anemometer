pipeline {
  agent any
       stages {
      stage('Semgrep-Scan') {
        steps {
            sh '''docker pull returntocorp/semgrep && \
            docker run \
            -e SEMGREP_APP_TOKEN=$SEMGREP_APP_TOKEN \
            -v "$(pwd):$(pwd)" --workdir $(pwd) \
            returntocorp/semgrep semgrep ci '''
      }
    }
  }
}
