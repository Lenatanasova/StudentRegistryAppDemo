pipeline{
    agent any

    stages{
        stage('Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/Lenatanasova/StudentRegistryAppDemo'
            }
        }

        stage('Install dependencies'){
            steps{
                script{
                        bat 'npm install'
                }
            }
        }

        stage('Start application and run tests'){
            steps{
                script{
                    bat 'start /b npm start'
                }
            }
        }

         stage('Run tests'){
            steps{
                script{
                    bat 'start npm test'
                }
            }
        }
    }

    post{
        always{
            echo "CI pipeline completed"
        }
    }
}