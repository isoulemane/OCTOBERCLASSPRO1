pipeline{
    tools{
        jdk 'myjava'
        maven 'mymaven'
    }
	agent any
      stages{
           stage('Checkout with git'){
              steps{
		 echo 'cloning..'
                 git 'https://github.com/isoulemane/OCTOBERCLASSPRO1.git'
              }
          }
          stage('Compile'){
              steps{
                  echo 'compiling..'
                  sh 'mvn compile'
	      }
          }
          stage('CodeReview'){
              steps{
		    
		  echo 'codeReview'
                  sh 'mvn pmd:pmd'
              }
          }
          
          stage('Package'){
              steps{
                  sh 'mvn package'
              }
          }
      }
}
