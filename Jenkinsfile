node{

    stage('SCM Checkout')
    {
        git url: 'https://github.com/jayadeep3/E-comm_App.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'docker-compose build'
        sh 'docker-compose up -d'
    }
  stage('PUSH image to Docker Hub')
    {
      /* withCredentials([string(credentialsId: 'DockerHubPassword', variable: 'DHPWD')]) 
        {
            sh "docker login -u jayadeep3 -p ${DHPWD}"
        }
        sh 'docker push vardhanns/phpmysql_app'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
             sh 'sudo docker login -u "jayadeep3" -p "Allu@1234" docker.io'
             //sh 'sudo docker push jayadeep3/mysql'
             //sh 'sudo docker push jayadeep3/job1_web1.0'
             sh 'sudo docker push jayadeep3/job1_web2.0'
            // sh 'docker push jayadeep3/mysql'
          
    }
}
