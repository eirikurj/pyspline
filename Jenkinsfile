pipeline {
    agent any



    stages {
        stage('clean_workspace_and_checkout_source') {
            steps {
            deleteDir()
            checkout scm
            sh 'env|sort'
            }
        }        
        stage('build') {
            steps {
                sh 'cd $MDOLAB_REPO_DIR'
                sh 'cp config/defaults/config.LINUX_GFORTRAN.mk config/config.mk'
                sh 'make'
                sh 'pwd'
                sh 'PYTHONPATH=$JENKINS_HOME/workspace'
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