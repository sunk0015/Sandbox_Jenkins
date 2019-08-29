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
                    println "Test ${env.WORKSPACE}"
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