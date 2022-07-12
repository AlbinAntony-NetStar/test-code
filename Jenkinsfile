pipeline 
{   
    environment
    {        
        APP_NAME = 'Indianmoney-codeigniter'
    }
    agent any
    stages 
    {
        stage('Cloning the App')
        {
            steps
            {
                checkout scm
                echo "${env.GIT_BRANCH}"
            }
        }
        stage('Rsync the app  directory')
        {
            steps
            {
                sh " rsync -av * /root/codeigniter  "
                sh " echo project running "
            
            }
        }
        
    }
}
