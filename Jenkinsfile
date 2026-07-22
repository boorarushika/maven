pipeline
{
    agent any
    stages
    {
        stage('Download_master')
        {
            steps
            {
                git 'https://github.com/IntelliqDevops/maven.git'
            }
        }
        stage('Build_master')
        {
            steps
            {
                sh 'mvn package'
            }
        }
        stage('Deploy_master')
        {
            steps
            {
                sh 'scp /var/lib/jenkins/workspace/DeclartivePipeline/webapp/target/webapp.war ubuntu@172.31.39.150:/var/lib/tomcat10/webapps/test1.war'
            }
        }
}	
