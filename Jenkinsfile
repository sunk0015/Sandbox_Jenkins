pipeline {
    agent any

    stages{


        stage('Git Checkout Sandbox Test'){
            steps{
                script{
                    def url = 'https://github.com/sunk0015/Sandbox_test'
                    checkout([$class: 'GitSCM', branches: [[name: '*/master']],
                        userRemoteConfigs: [[url: url]]])
                }
            }
        }
        
        stage('Test'){
            steps{
                script{
                    sh "python ${env.WORKSPACE}/hello.py"
                }
            }
        }

        stage('Deploy to UAT'){
            steps{
                script{
                    println 'Deploy to UAT'
                }
            }
        }

        stage('Deploy to Prod'){
            steps{
                script{
                    println 'Deploy to Prod'
                }
            }
        }
    }
    
}