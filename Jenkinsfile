pipeline{
    agent any
    environment{
        DIRECTORY_PATH = "/Users/kaviyarammanaiken/.jenkins/workspace/continuous_delivery_pipeline"
        TESTING_ENVIRONMENT = "Jenkins"
        PRODUCTION_ENVIRONMENT = "Kaviya"
    }
    stages{
        stage('Build'){
            steps{
                echo "fetch the source code from the directory path ${env.DIRECTORY_PATH}"
                echo "compile the code and generate any necessary artifacts"
            }
        }
        stage('Test'){
            steps{
                echo "unit tests"
                echo "integration tests"
            }
        }
        stage('Code Quality Check'){
            steps{
                echo "Checking the code quality"
            }
        }
        stage('Deploy'){
            steps{
                echo "deploy the application to the testing environment ${env.TESTING_ENVIRONMENT}"
            }
        }
        stage('Approval'){
            steps{
                echo "Waiting for approval..."
                sleep 10
                echo "Approval received, continuing with the pipeline."
            }
        }
        stage ('Deploy to Production'){
            steps{
                echo "Deploy the code to the production environment ${env.PRODUCTION_ENVIRONMENT}"
            }
        stage ('Close'){
            steps{
                echo "Closing the program"
        }
    }
}
