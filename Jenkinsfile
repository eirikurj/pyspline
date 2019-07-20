pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'cd $MDOLAB_REPO_DIR'
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