pipeline {
    agent { docker { image 'mdolab/regtest:s1' } }
    stages {
        stage('build') {
            steps {
                sh 'pwd'
                sh 'python --version'
                sh 'echo $PATH'
                sh 'echo $USER'
                sh 'env'
                sh 'echo $MDOLAB_REPO_DIR'
                sh 'cp config/defaults/config.LINUX_GFORTRAN.mk config/config.mk'
                sh 'make'
                sh 'pwd'
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