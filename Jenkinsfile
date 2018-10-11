pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                //sh 'git clone https://github.com/lnxlalith/base_java8.git'
                //sh 'git clone https://github.com/lnxlalith/base_postgres.git'
                    //sh 'ansible-playbook artifactory-playbook/requirements.yml'
                //sh 'ansible-galaxy install -r artifactory-playbook/requirements.yml'
                //sh 'ansible-playbook -i artifactory-playbook/inventory artifactory-playbook/playbook.yml'
                //sh 'ansible-playbook -i maven-playbook/inventory maven-playbook/maven.yml'
                //sh 'ansible-playbook -i sonar-playbook/inventory sonar-playbook/sonar.yml'
                sh 'ansible-playbook -i tomcat-playbook/inventory tomcat-playbook/tomcat.yml -k -e ansible_python_interpreter=/usr/bin/python2.7'
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
