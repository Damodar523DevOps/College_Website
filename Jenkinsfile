pipeline {
    agent any

    stages {
        stage("build") {
            steps {
                echo 'Building package using Maven'
                sh 'mvn clean package'
            }
        }
        stage('Verify Package') {
            steps {
                echo 'Checking generated packages'

                sh 'ls -lh target/'
             }
        }
        stage('Build Success') {
            steps {
                
                echo 'Maven package generated successfully!'
             }
        }
        stage("test") {
            steps {
                echo 'It is from test stage'
            }
        }

        stage("deploy") {
            steps {
                echo 'It is from Deploy stage'
            }
        }
    }
}
