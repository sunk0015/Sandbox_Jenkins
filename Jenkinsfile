pipeline {
    agent any

    stages{


        stage('SCM'){
            steps{
                script{
                    println 'SCM'
                }
            }
        }
        
        stage('Test'){
            steps{
                script{
                    println 'Test'
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