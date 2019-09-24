pipeline {
    agent {
        dockerfile {
            filename 'AnsibleDockerFile.Ubuntu18'
        }
    }
    stages {
      stage('GitHub') {
          steps {
              echo 'Running GitHub Stage'
              git credentialsId: '93924462-8163-4fbd-9d28-39567c887825', url: 'https://github.com/BecherX64/Hello-Project-Repo'
          }   
      }
      
      stage('script') {
          steps {
            echo 'Running Scrits stage'
            echo 'hostname:'
            sh "hostname"
            echo 'existing users:'
            sh "cat /etc/passwd"
            echo 'current dir:'
            sh "pwd"
            echo 'List files in current dir'
            sh "ls -al"
          }
      }
      stage ('RunPing') {
          steps {
              echo 'Running Ansible Ping'
              sh "ansible all -m ping"
          }    
      }      
      stage ('Ansible') {
          steps {
              echo 'Running Ansible stage'
              echo 'Ansible Version:'
              sh "ansible --version"
              echo 'Running ansible playbook:'
              ansiblePlaybook colorized: true, playbook: 'getinfo.yml', inventory: 'inventory.list'
          }
      }
    }
}
