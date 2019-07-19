pipeline {
    agent { docker { image 'mdolab/regtest:s1' } }
    stages {
        stage('build') {
            steps {
                sh 'docker exec -it mdolab/regtest:s1 /bin/bash -c "pwd; cd $MDOLAB_REPO_DIR"'
                sh 'cd $MDOLAB_REPO_DIR'
                sh 'cp config/defaults/config.LINUX_GFORTRAN.mk config/config.mk'
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