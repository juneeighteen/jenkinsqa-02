properties([buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '', numToKeepStr: '5')), pipelineTriggers([])])

node {
    stage ('Hello') {
	    sh 'echo hello world'
    }

   milestone label: 'start-deploy', ordinal: 1
   stage('Deploy') {
        sh 'echo I deploy all the things'
        lock('test-resource') {
            sleep 120
            echo "That was a nice nap"
        }
        lock(inversePrecedence:true, 'second-resource') {
            sleep 120
            echo "Another great nap"
        }

   }
}
