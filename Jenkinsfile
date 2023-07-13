pipeline {
    agent any

    stages {
        stage('git') {
            steps {
               checkout scm
            }
        }
         stage('ansible-playbook') {
            steps {
                ansiblePlaybook colorized: true, become: true, credentialsId: 'root', extras: 'op_type=started', disableHostKeyChecking: true, installation: 'ansible', inventory: 'inventory.yml', playbook: 'docker.yml'
            }
        }
    }
}
