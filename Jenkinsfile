node {
    git branch: 'main', url: 'https://github.com/ZiadSamehShehawy/Yummy_Food.git'

    stage('build') {
        try {
            sh 'echo "elzoz is top"'
        } catch(Exception e) {
            sh 'echo "mohab is top"'
            throw e
        }
    }

    stage('test') {
        if (env.BRANCH_NAME == 'feature') {
            sh 'echo "test"'
        } else {
            sh 'echo "skip test stage"'
        }
    }
}