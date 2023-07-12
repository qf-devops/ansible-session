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
                sh "ansible-playbook -i inventory.yml webserver.yml"
            }
        }
    }
}
