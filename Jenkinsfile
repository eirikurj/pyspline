pipeline {
    agent { docker { image 'mdolab/regtest:s1' } }
    stages {
        stage('build') {
            steps {
                sh 'echo $MDOLAB_REPO_DIR'
                sh 'cd $MDOLAB_REPO_DIR'
                sh 'cp config/defaults/config.LINUX_INTEL.mk config/config.mk'
                sh 'make'
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