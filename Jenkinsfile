pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                echo "Building ..."
            }
        }
        post{
            success{
                mail to: "kaviyarammanaiken098@gmail.com",
                subject: "Build Status Email",
                body: "Build was successful!"
            }
        }
    }
}    
  
