pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'mvn clean package' //generate the .war file
                bat "docker build . -t tomcatwebapp:${env.BUILD_ID}" // call docker which will open dockerfile, and generate a tag and versioned Docker image
            }
        }
    }
}