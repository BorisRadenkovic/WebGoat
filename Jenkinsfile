
@Library('Jenkins-shared-library') _

pipeline {
    
    agent any
//enviroment {
    //PATH = "/usr/share/maven:$PATH"
          
//}
    

    stages {
        stage('CLONE') {
            steps {
                
               script{
                
                 //   clone.cloneRepo()
                   
                   clone.cloneRepo("https://github.com/brki18/devops_web_goat", "*/master", "MyGithub")
                }
                
             //  git branch: 'master', credentialsId: 'MyGithub', url: 'https://github.com/brki18/devops_web_goat'
            }
        }
        
        stage('BUILD') {
                              
            steps {
              //  dir ("devops_web_goat"){
              //  sh "mvn clean install -DskipTests"
                script{
                build.cleanInstall()
                }
            }
            
       
      }
    //   stage('GETJar') {
      //      steps {
       //         sh "sudo cp /var/lib/jenkins/workspace/Webgoat-pipeline/webgoat-server/target/webgoat-server-v8.1.0.jar /home/rboris" 
                
         //   }
      //  }
    //    stage('STARTApp') {
      //      steps {
      //          sh "nohup java -jar /home/rboris/webgoat-server-v8.1.0.jar --server.port=8081 --server.address=localhost > /dev/null 2>&1 &"
                   // x-www-browser http://localhost:8081/webgoat
        //   }
        
     //  }
    
    }
}

