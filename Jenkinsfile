pipeline{
    agent any
    stages {
    
        stage('Setup Python Virtual ENV'){
       
      steps  {
            sh '''
            chmod +x env_setup.sh
            ./env_setup.sh
            '''}
        }
        stage('Setup Gunicorn Setup'){
            steps {
                sh '''
                chmod +x gunicorn/gunicorn.sh
                ./gunicorn/gunicorn.sh
                '''
            }
        }
        stage('setup NGINX'){
            steps {
                sh '''
                chmod +x nginx/nginx.sh
                ./nginx/nginx.sh
                '''
            }
        }
    }
}