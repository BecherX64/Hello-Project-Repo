node('ansible') {
    // some block
    stage('echo') {
        // some block
        echo 'Hello-World'
    }
    stage('script') {
        // some block
        echo 'hostname:'
        sh "hostname"
        echo 'current dir:'
        sh "pwd"
    }
    stage('GitHub') {
        git credentialsId: '93924462-8163-4fbd-9d28-39567c887825', url: 'https://github.com/BecherX64/Hello-Project-Repo'
    }
}
