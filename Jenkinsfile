pipeline {
agent any
stages {
stage(’Build’) {
steps {
sh ’ls’
}
steps {
npm install
}
steps {
npm install grunt-cli
}
steps {
./node_modules/grunt-cli/bin/grunt
}
}
post {
always {
archiveArtifacts artifacts: ’path/to/*._less.github.io’,
fingerprint: true
}
}
}
