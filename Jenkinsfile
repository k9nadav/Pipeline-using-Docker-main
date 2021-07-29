pipeline {
    agent any
	
	//  tools
  //  {
   //    maven "Maven"
   // }
 stages {
      stage('checkout') {
           steps {
             
                git branch: 'main', url: 'https://github.com/oralabuser/Pipeline-using-Docker.git'
             
          }
        }
	 stage('Execute Maven') {
           steps {
             
                sh 'mvn package'             
          }
        }
        

  stage('Docker Build and Tag') {
           steps {
              
                sh 'docker build -t samplewebapp:latest .' 
                sh 'docker tag samplewebapp dockerdemo/samplewebapp:latest'
                //sh 'docker tag samplewebapp dockerdemo/samplewebapp:$BUILD_NUMBER'
               
          }
        }
     
  //stage('Publish image to Docker Hub') {
          
  //          steps {
  //    withDockerRegistry([ credentialsId: "dockerHub", url: "" ]) {
  //        sh  'docker push dockerdemo/samplewebapp:latest'
        //  sh  'docker push dockerdemo/samplewebapp:$BUILD_NUMBER' 
   //     }
                  
   //       }
   //     }
     
      //stage('Run Docker container on Jenkins Agent') {
             
         //   steps 
	//		{
         //       sh "docker run -d -p 8003:8080 dockerdemo/samplewebapp"
 
        //    }
      //  }
// stage('Run Docker container on remote hosts') {
             
        //    steps {
        //        sh "docker -H ssh://oralabuser@52.66.28.111 run -d -p 8002:8080 dockerdemo/samplewebapp"
 
        //    }
      // }
    }
	}
    
