pipeline {
agent any
stages {
stage('Build') {
steps {
sh 'ls' 
}
steps {
sh 'npm install'
}
steps {
sh 'npm install grunt-cli'
}
steps {
sh './node_modules/grunt-cli/bin/grunt'
}
}
post {
always {
archiveArtifacts artifacts: 'path/to/*._less.github.io',
fingerprint: true
}
}
}

