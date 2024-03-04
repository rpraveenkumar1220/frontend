pipeline {
    agent { label 'workstation'}
    stages {
        stage('Unit Test'){
         steps { echo "Unit testing"  }
         }
        stage('Code Analysis'){
        steps {
        echo "Code Analysis"sh
        sh 'sonar-scanner -Dsonar.host.url=http://172.31.10.14:9000  -Dsonar.login=admin -Dsonar.password=admin123 -Dsonar.projectKey=frontend -Dsonar.qualitygate.wait=true'
            }
             }
        stage('Security Scans'){
        steps { echo "Security Scans" }
        }
        stage('Publish Artifacts'){
        steps { echo "Publish Artifacts" }
        }
            }
           }
