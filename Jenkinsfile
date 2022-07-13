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

        stage('Backup Doc')
        {
            steps
            {
                sh " cp -r /root/codeigniter/ /root/backup/codeigniter."${date}" " 
            }
        }

        stage('Rsync to the app  directory')
        {
            steps
            {
                sh " rsync -av * /root/codeigniter  "
            
            }
        }
        
    }
}

