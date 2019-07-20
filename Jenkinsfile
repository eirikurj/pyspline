pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'cd $MDOLAB_REPO_DIR'
                sh 'cp config/defaults/config.LINUX_GFORTRAN.mk config/config.mk'
                sh 'make'
                sh 'pwd'
                sh 'env'
            }
        }
        stage('test') {
            steps {
                sh 'cd python/reg_tests; python run_reg_tests.py -nodiff'
            }
        }        
    }
}