node {
    stage("Checking out") {
        checkout scm
    }

    stage("Deploying to artifactory") {
        withMaven(maven: 'maven'){
            sh 'mvn clean deploy:deploy'
        }
    }

}