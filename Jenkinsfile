pipeline{
    agent any
    tools{
        maven "MAVEN3"
        jdk "jdk8"
    }

    environment {
        SNAP_REPO = 'viprofile-snapshot'
        NEXUS_USER = 'admin'
        NEXUS_PASS = 'admin@123'
        RELEASE_REPO = 'viprofile-release'
        CENTRAL_REPO = 'vipro-maven-central'
        NEXUSIP = '172.31.18.135'
        NEXUSPORT = '8081'
        NEXUS_GRP_REPO = 'vipro-maven-group'
        NEXUS_LOGIN = 'nexuslogin'
        SONARSERVER = 'sonarserver'
        SONARSCANNER = 'sonarscanner'

    }
    stages{
        stage('Build'){
            steps{
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }  
    }    
}