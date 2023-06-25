/* groovylint-disable-next-line CompileStatic */
pipeline {
    agent any
    environment {
        RELEASE = '20.04'
    }

    stages {
        stage('build') {
            agent any
            environment {
                LOG_LEVEL = 'INFO'
            }
            steps {
                /* groovylint-disable-next-line GStringExpressionWithinString */
                echo 'building relatse $RELEASE with log ${LOG_LEVEL}'
            }
        }

        stage('test') {
            steps {
                echo "BUILDING $RELEASE BUT NOT LOG $LOG_LEVEL"
            }
        }
    }
}
