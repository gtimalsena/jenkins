pipeline {
    agent any 
    stages{
        stage('test'){
            agent { label 'linux' }
            steps{
                deleteDir()
                sh 'mkdir -p archive'
                sh 'echo test > archive/test.txt'
                script{
                    zip archive: true, dir: 'archive', glob: '', zipFile: 'coverage1-files.zip'
                } 
            }
        }
    }
}
