pipeline {
    agent any
    stages {
  	stage ('Prepare') {
        steps {
            checkout([$class: 'GitSCM', 
                branches: [[name: '*/master']], 
                extensions: [[$class: 'CleanCheckout']], 
                userRemoteConfigs: [[credentialsId: 'git-credentials', url: 'https://github.com/MrudhulaRani/jenkins/tree/master/assignment_mail.git']]
                ])
            }
        }
        stage('buid') {
            steps {
                sh 'npx create-react-app my-app-Hello-world"'
            }
		}
        stage('deploy') {
            steps {
                sh 'cd my-app-Hello-world'
                sh 'npm start'
            }
			}
        }
        }
