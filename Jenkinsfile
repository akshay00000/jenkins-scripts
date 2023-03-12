pipeline{

agent{

    label{

           label "built-in"
           customWorkspace "/mnt/project-8"





    }





}

stages {

stage('SCM'){

     steps{
         sh "rm -rf /mnt/project-8/game-of-life"
         sh  "yum install git -y"
         sh  "git clone https://github.com/akshay00000/game-of-life.git"
         



     }



}

stage('BUILD'){
  steps{

       dir ('/mnt/project-8/game-of-life'){

        sh "yum install maven -y"
        sh "mvn clean install"
        

           


       }



  }



}  

stage('DEPLOY'){

steps{

    sh "cp -r /mnt/project-8/game-of-life/gameoflife-web/target/gamoflife.war /opt/server/apache-tomcat-9.0.71/webapps" 




}



}


}


}
