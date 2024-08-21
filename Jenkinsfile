pipeline{

    agent any

        stages{
            stage('Git Checkout'){
                steps{
                    git branch: 'main', url: 'https://github.com/olanrewajuremi/demo-counter-app.git'
                }
            }
            stage('MVN Testing'){
                steps{
                    sh 'mvn test'
                }
            }
            stage('Integration Testing'){
                steps{
                    sh 'mvn verify -DskipUnitTests'
                }
            }
        }
}