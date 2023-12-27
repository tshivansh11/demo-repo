pipeline {
    agent any
    stages {
        stage('Test') {
            parallel {
                stage('Checkout') {
                    steps {
                        checkout(scm)
                    }
                }
                stage('Maven test') {
                    steps {
                        echo 'testing to the any test case'
                        sh "mvn test"
                    }
                }
                stage('Maven install') {
                    steps {
                        echo 'creating .war file'
                        sh "mvn install"
                    }
                }
            }
        }
    }
}
