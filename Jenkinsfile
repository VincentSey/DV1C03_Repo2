pipeline {
    agent any
    stages {
       stage('Stage1_22053098') {
           steps {
               echo "S1_22053098 : Environment Preparation Completed"
           } 
       }
        
       stage('Stage2_22053098') {
           steps {
               sh(script:"""
                    docker run -d -it -p 42000:8080 --name=s2_22053098_server 22053098_webimage /bin/sh
                    docker rm -f s2_22053098_server
                """)
                echo "s2_22053098 : Web Server Creation Completed"
           }
       }
       
      stage('Three and Four'){
          parallel{
              stage('Stage3_22053098') {
                 steps {
                    echo "S3_22053098 : API Test Completed"
                 } 
              }   
              stage('Stage4_22053098') {
                 steps {
                    echo "S4_22053098 : Dast Security Test Completed"
                 } 
              }  
          }
      }
 
      stage('Stage5_22053098') {
           steps {
               input('Do you want to release the work?') 
           } 
       }
       
       stage('Stage6_22053098'){
           steps{
                 echo "Work Released - 22053098"  
           }
       }
    }
}
