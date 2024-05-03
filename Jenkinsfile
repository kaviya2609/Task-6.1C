pipeline
{
    agent any
    stages
    {
        // Stage 1
        stage("Build")
        {
            steps
            {
                echo "Building using Maven"
            }
        }
        // Stage 2
        stage("Unit and Integration Tests")
        {
            steps
            {
                echo "Running unit tests using JUnit"
                echo "Running integration tests using JUnit"
            }
            post
            {
                success
                {
                    mail to: "kaviyarammanaiken098@gmail.com",
                    subject: "Tests Status Email",
                    body: "Tests were successful!"
                    attachLog: true
                }
            }
        }
       
        // Stage 3
        stage("Code Analysis")
        {
            steps
            {
                echo "Analysing code using SonarQube"
            }
        }
        // Stage 4
        stage("Security Scan")
        {
            steps
            {
                echo "Scanning for security vulnerabilities using OWASP ZAP"
            }
            post
            {
                success
                {
                    mail to: "kaviyarammanaiken098@gmail.com",
                    subject: "Security Scan Status Email",
                    body: "Security Scan was successful!"
                    attachLog: true
                }
            }
        }
        // Stage 5
        stage("Deploy to Staging")
        {
            steps
            {
                echo "Deploying to staging server AWS EC2"
            }
        }
        // Stage 6
        stage("Integration Tests on Staging")
        {
            steps
            {
                echo "Running integration tests on staging environment using JUnit"
            }
        }
        // Stage 7
        stage("Deploy to Production")
        {
            steps
            {
                echo "Deploying to production server AWS EC2"
            }
        }
    }
}     
