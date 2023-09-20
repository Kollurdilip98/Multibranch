pipeline
{
    agent any
    
    stages()
    {
        stage('download')
        {
            steps()
            {
                git 'https://github.com/Kollurdilip98/Developer-Code.git'
            
            }
              }
        stage('build')
        {
            steps()
            {
                sh 'mvn package'
            }
        }
        
        stage('deployment')
        {
            steps()
            {
                deploy adapters: [tomcat9(credentialsId: 'none', path: '', url: 'http://54.81.238.2:8080/')], contextPath: 't', war: '**/*.war'
            }
        }
        
        stage('test')
        {
            steps()
            {
                git 'https://github.com/Kollurdilip98/Testing-Code.git'
            sh 'java -jar  /var/lib/jenkins/workspace/Declarative/testing.jar'
            }
        }
        
           
         
    }
}  
