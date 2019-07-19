pipeline {
    agent { docker { image 'mdolab/regtest:s1' } }
    stages {
        stage('build') {
            steps {
                sh 'echo $MDOLAB_REPO_DIR'
                sh 'cd $MDOLAB_REPO_DIR'
                sh 'pwd'
                sh 'ls -la'
            }
        }
        stage('test') {
            steps {
                sh 'echo $MDOLAB_REPO_DIR'
                sh 'cd $MDOLAB_REPO_DIR'
            }
        }        
    }
}