node {
    stage("Checking out") {
        checkout scm
    }

    stage("Deploying to artifactory") {
        withMaven(maven: 'maven'){
            sh 'mvn clean package deploy:deploy'
        }
    }

}