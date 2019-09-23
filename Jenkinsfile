//node('ansible') {
    // some block
pipeline {
    agent {
        dockerfile {
            filename 'Ansible.Dockerfile'
        }
    }
    stage('echo') {
        // some block
        echo 'Hello-World'
    }
    stage('GitHub') {
        git credentialsId: '93924462-8163-4fbd-9d28-39567c887825', url: 'https://github.com/BecherX64/Hello-Project-Repo'
    }
    stage('script') {
        // some block
        echo 'hostname:'
        sh "hostname"
        echo 'current dir:'
        sh "pwd"
    }
    stage ('Ansible') {
        //ansiblePlaybook colorized: true, credentialsId: '7b612a74-a2af-4be7-8338-f565bf54ead9', playbook: 'testplaybook.yml'
    }

}
