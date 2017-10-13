# jenkins-docker-gc

Coordinates running Docker garbage collection on all Jenkins slaves

## Setup

Kind of unfortunately, this requires that two jobs within your Jenkins cluster be setup.

1. A coordination job (named whatever you'd like) which uses a "Pipeline script from SCM" and a script path of `all_agent_kickoff.groovy`
* A `spotify-docker-gc` job with a script path of `Jenkinsfile`
