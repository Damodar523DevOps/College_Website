pipeline {
    agent any

    stages {
        stage("Build") {

            echo 'Building package using Maven'

            def mvnHome = tool 'Maven-3'

            withEnv(["PATH+MAVEN=${mvnHome}/bin"]) {

                sh 'mvn -version'

                sh 'mvn clean package'
            }
       }

       stage("Verify Package") {
        sh 'find . -type f \\( -name "*.jar" -o -name "*.war" \\)'
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
