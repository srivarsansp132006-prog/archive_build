pipeline{
    agent any
    stages{
        stage('Checkout') {
            steps{
                gitbranch: 'main', url: 'https://github.com/srivarsansp132006-prog/archive_build.git'
            }
        }
        stage('GenerateReport') {
            steps{
                bat 'python app.py'
            }
        }
        stage('ArchiveReport'){
            steps{
                archiveArtifactsartifacts: 'report.txt',fingerprint:true
            }
        }
    }
}