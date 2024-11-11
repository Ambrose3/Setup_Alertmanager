pipeline {
    agent any

    environment {
        ANSIBLE_PLAYBOOK = 'alertmanager.yml'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Run setup alertmanager') {
            steps {
                script {
                    // Run the Ansible playbook
                    sh "ansible-playbook ${ANSIBLE_PLAYBOOK}"
                }
            }
        }
    }
}
