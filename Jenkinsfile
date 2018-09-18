pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                //sh 'git clone https://github.com/lnxlalith/base_java8.git'
                //sh 'git clone https://github.com/lnxlalith/base_postgres.git'
                //sh 'ansible-playbook artifactory-playbook/requirements.yml'
                sh 'ansible-galaxy install -r artifactory-playbook/requirements.yml'
                sh 'ansible-playbook -i artifactory-playbook/inventory artifactory-playbook/playbook.yml'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
