pipeline{
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
}