pipeline {
    agent any
    environment{
        name='jyoti'
    }

    stages {
        stage('test') {
            steps {
                sh 'date'
                sh 'pwd'
                echo  'test Hello World'
            }
        }
        stage('build') {
            steps {

                sh'''
                 date
                 ls
                 pwd
                '''
                echo 'build Hello World'
            }
        }
        stage('deploy test evironment') {
            
            steps {
                   echo 'deploy test Hello World'
                   sh 'echo "${BUILD_ID}"'
                   sh 'echo "${name}"'
            }
        }
        stage('deploy prod') {
            steps {
                echo 'deploy prod Hello World'
            }
        }
    }
     post { 
        always { 
            echo 'I will always say Hello again!'
        }
         success { 
            echo 'successful'
        }
         failure { 
            echo 'failed!'
        }
     }
}
