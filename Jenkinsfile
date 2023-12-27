node('built-in')
{
  stage('cd')
  {
    try
    {
    git 'https://github.com/Kollurdilip98/Developer-Code.git'
    }
    catch (Exception e1)
    {
      
    }
  }
  stage('cb')
  {
    sh 'mvn package'
  }
  stage('cd')
  {
        sh 'scp /var/lib/jenkins/workspace/Scripted/webapp/target/webapp.war ubuntu@54.159.216.212:/var/lib/tomcat9/webapps/t.war'
    
  }
  stage('ct')
  {
    git 'https://github.com/Kollurdilip98/Testing-Code.git'
     sh 'java -jar /var/lib/jenkins/workspace/Scripted/testing.jar'

  }
  stage('cd')
  {
     sh 'scp /var/lib/jenkins/workspace/Scripted/webapp/target/webapp.war ubuntu@54.234.122.191:/var/lib/tomcat9/webapps/p.war'

  }
}
