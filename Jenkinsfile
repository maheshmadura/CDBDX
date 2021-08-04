pipeline{
    agent any
    stages{
           stage('clone repo')
           {
               steps{                      sh "rm -rf CDBDX" 
                                           sh "git clone https://github.com/maheshmadura/CDBDX.git"
					   sh "mvn clean -f CDBDX"
                   
                    }
               
           }
           stage('testing')
           
           {
               steps{
                        sh 'mvn test -f CDBDX'
                    }
           }
           
            stage('Deployment stage')
           
           {
               steps{
                        sh 'mvn package -f CDBDX'
                    }
           }
        
        
    }
}





stages {
  steps('xyz') {
    dir('/opt/tools') {
       sh "pwd"
    }
  }
}
