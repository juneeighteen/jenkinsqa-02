properties([buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '', numToKeepStr: '10')), pipelineTriggers([])])

node {
    stage ('Hello') {
	    sh 'echo hello world'
    }
}
