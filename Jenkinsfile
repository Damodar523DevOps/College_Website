pipeline {
    agent any
    tools {
        maven 'Maven-3'
    }
    stages {
        stage("Build") {
            steps {
                echo 'Building package using Maven'

                    sh 'mvn -version'

                    sh 'mvn clean package'
            }
        }

        stage("Verify Package") {
        
            steps {
                echo 'Verifying generated packages'
                sh 'find . -type f \\( -name "*.jar" -o -name "*.war" \\)'
            }
        }    
        stage("Build Success") {
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
