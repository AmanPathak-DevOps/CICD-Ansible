pipeline {
    agent any 
    stages {
        stage('Preparing') {
            step {
                sh 'echo Preparing'
            }
        }
        stage('Git Pulling') {
            step{
                git branch: 'master', url: 'https://github.com/AmanPathak-DevOps/CICD-Ansible.git'
            }
        }
        stage('Playbook Initializing') {
            step{
                sh 'echo Playbook Initializing'
            }
        }
        stage('Playbook Running') {
            step{
                ansiblePlaybook credentialsId: 'ansible-connect', disableHostKeyChecking: true, inventory: '/etc/ansible/hosts', playbook: 'Nginx-Uninstallation.yml'
            }
        }
        stage('Playbook deployed') {
            step{
                sh 'echo Deployment done!!!!'
            }
        }
    }
}