pipeline {
    agent any


    environment {
        PYTHONPATH= $(pwd):$PYTHONPATH
    }

    stages {
        stage('clean_workspace_and_checkout_source') {
            steps {
            deleteDir()
            checkout scm
            }
        }        
        stage('build') {
            steps {
                sh 'cd $MDOLAB_REPO_DIR'
                sh 'cp config/defaults/config.LINUX_GFORTRAN.mk config/config.mk'
                sh 'make'
                sh 'pwd'
                sh 'env | sort'
            }
        }
        stage('test') {
            steps {
                sh 'cd python/reg_tests; python run_reg_tests.py -nodiff'
            }
        }        
    }
}