pipeline
{
    agent any
    
    stages
    {
        stage('Build')
        {
            steps
            {
                echo 'Build App'
            }
        }
        
        stage('Test')
        {
            steps
            {
                echo 'Test App'
            }
        }
        
        stage('Deploy')
        {
            steps
            {
                echo 'Deploy app'
            }
        }

        post
        {
        failure
        {
            emailext body: 'summery', recipientProviders: [contributor()], subject: 'pipeline status', to: 'basava.tarun@gmail.com'
        }
    }
}
