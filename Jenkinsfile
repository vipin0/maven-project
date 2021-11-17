pipeline{
    agent any
    tools{
        maven 'Maven'
    }
    stages{
        stage('build jar'){
            steps{
                sh 'mvn clean package'
            }
        }
    }
    post{
        success{
            archiveArtifacts artifacts: '**/target/*.war', followSymlinks: false
        }
    }
}