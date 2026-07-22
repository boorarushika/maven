pipeline
{
    agent any
    stages
    {
        stage('Download_loans')
        {
            steps
            {
                git 'https://github.com/IntelliqDevops/maven.git'
            }
        }
        stage('Build_loans')
        {
            steps
            {
                sh 'mvn package'
            }
        }
        stage('Deploy_loans')
        {
            steps
            {
                sh 'scp /var/lib/jenkins/workspace/DeclartivePipeline/webapp/target/webapp.war ubuntu@172.31.39.150:/var/lib/tomcat10/webapps/test1.war'
            }
        }
}	
