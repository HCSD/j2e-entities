node {
    stage("Checking out") {
        checkout scm
    }

    stage("Deploying to artifactory") {
        withMaven(
            maven: 'maven',
            mavenSettingsConfig: 'maven'){
            sh 'mvn clean package deploy:deploy'
        }
    }

    stage("Fingerprinting") {
        fingerprint ''
    }

}