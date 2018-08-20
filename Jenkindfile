pipeline {
agent any
stages {
stage(’Build’) {
steps {
sh ’ls’
}
}
}
post {
always {
archiveArtifacts artifacts: ’path/to/*.jar’,
fingerprint: true
}
}
}
