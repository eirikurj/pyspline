pipeline {
    agent any

    stages {

        stage('py2_real_build') {
            steps {
                sh 'cp config/defaults/config.LINUX_GFORTRAN.mk config/config.mk'
                sh '. /home/mdolab/packages/setMdolabPath; conda activate py2; env|sort; make'
            }
        }

        stage('py2_real_test') {
            steps {
                sh '. /home/mdolab/packages/setMdolabPath; conda activate py2; env|sort; cd python/reg_tests; python run_reg_tests.py -nodiff'
            }
        }            
    }
}