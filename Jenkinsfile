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
               sh " cd test-code && git pull  " 
            }
        }

        stage('Backup Doc')
        {
            steps
            {
               sh " cp -r /root/codeigniter /root/backup/codeigniter " 
            }
        }

        stage('Rsync to the app  directory')
        {
            steps
            {
                sh " cd test-code && rsync -av * /root/codeigniter  "
            
            }
        }
        
    }
}

