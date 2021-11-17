pipeline{
    agent any
    tools{
        maven 'Maven'
    }
    stages{
        stage('build war'){
            steps{
                echo "Building war file"
                sh 'mvn clean package'
            }
        }
        stage('build docker image'){
            echo "Buildind docker image"
            sh 'docker build -t java-mvn:0.1 .'
        }
        stage('deploy'){
            echo "Deploying application"
        }
    }
    post{
        success{
            archiveArtifacts artifacts: '**/target/*.war', followSymlinks: false
        }
    }
}