// This is setup as a separate job named 'spotify-docker-gc'
// which matches the job specified in the kickoff script
pipeline {
    agent { node { label "$TARGET_NODE" } }
    stages {
        stage('Pull latest image') {
            steps {
                sh 'docker pull spotify/docker-gc'
            }
        }
        stage('Run docker-gc') {
            steps {
                sh 'docker run --rm -v /var/run/docker.sock:/var/run/docker.sock spotify/docker-gc'
            }
        }
    }
}
