pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Bulding or Resolve Dependencies!'
                sh 'bundle install'
            }
        }
        stage('Test') {
            steps {
                echo 'Running regression tests'
            }
        }
        stage('UAT'){
            steps {
                echo 'Wait for User Accpetance'
                input(message: 'Go to production?', ok: 'Yes')
            }
        }
        stage('Prod'){
            steps {
                echo 'WebApp is Ready :)'
            }
        }
    }
}