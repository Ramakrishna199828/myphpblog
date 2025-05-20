pipeline {
    agent any
    
    stages {

        stage('clone from git hub repository') {

            steps {
                echo "Clonig the code from git hub repository"
                git 'https://github.com/Ramakrishna199828/myphpblog.git'
            }

        }

        stage('Deploy to Apache') {

            steps {

                sh '''

                echo "Copy complted from jenkins workspca to apache root folder"
                sudo cp -r * /var/www/html/
                
                echo "Changed the user/group persimission for apache"
                sudo chown -R www-data:www-data /var/www/html/
                
                echo "Changed the files& folder permissions"
                sudo chmod -R 755 /var/www/html/

                echo "Deployment completed successfully"                

                '''

            }

        }

    }
}


