pipeline {
    agent any

    stages{


        stage('Git Checkout Sandbox Test'){
            steps{
                script{
                    def url = 'https://github.com/sunk0015/Sandbox_test'
                    checkout([$class: 'GitSCM', branches: [[name: '*/']],
                        userRemoteConfigs: [[url: url]]])
                }
            }
        }
        
        stage('Test Master'){
            steps{
                script{
                    sh "git checkout master"
                    sh "python ${env.WORKSPACE}/hello.py"
                }
            }
        }

        stage('Test dev'){
            steps{
                script{
                    sh "git checkout dev"
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