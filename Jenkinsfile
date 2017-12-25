// This is setup as a separate job named 'docker-gc'
// which matches the job specified in the kickoff script
pipeline {
    agent { node { label "$TARGET_NODE" } }
    stages {
        stage('Prune') {
            steps {
                sh 'docker system prune --all --force'
            }
        }
    }
}
