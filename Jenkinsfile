pipeline {
    agent any

    stages {
        stage('Checkout SCM') {
            steps {
                git 'https://github.com/Fairez-Rashid/C300-FYP.git'
                
            }
        }

        stage('Maven compile') {
            steps {
                sh "mvn clean build"
            }
        }

        stage('Maven package') {
            steps {
                sh "mvn package -Dmaven.test.skip=true"
            }
        }

        // stage('Archive artifacts') {
        //     steps {
        //         archiveArtifacts artifacts: '**/*.war', onlyIfSuccessful: true
        //     }
        // }

        // stage('Archive Test Results') {
        //     steps {
        //         junit allowEmptyResults: true, testResults: '**/surefire-reports/*.xml'
        //     }
        // }

        // stage('Deploy') {
        //     steps {
        //         withCredentials([[
        //             $class: 'UsernamePasswordMultiBinding',
        //             credentialsId: 'your-credentials-id',
        //             usernameVariable: 'USERNAME',
        //             passwordVariable: 'PASSWORD'
        //         ]]) {
        //             sh 'scp -o StrictHostKeyChecking=no -r target/*.war USERNAME:PASSWORD@remote-server:/path/to/deploy/'
        //         }
        //     }
        // }
    }
}
