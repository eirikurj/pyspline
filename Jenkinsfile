pipeline {
    agent { docker { image 'mdolab/regtest:s1' } }
    stages {
        stage('build') {
            steps {
                echo $MDOLAB_REPO_DIR
                cd $MDOLAB_REPO_DIR
            }
        }
        stage('test') {
            steps {
                echo $MDOLAB_REPO_DIR
                cd $MDOLAB_REPO_DIR
            }
        }        
    }
}