pipeline {

    agent any

    stages {
        stage('Checkout') {
            steps {
                deleteDir()
                // checkoutout repository contents to the working directory
                checkout scm
            }
        }

        stage('Build') {
            steps {
                withMaven() {
                    sh 'mvn clean install'
                }
            }
        }

    }

}