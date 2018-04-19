pipeline {
   agent { docker { image 'maven:3.5-alpine' } }

   options {
      buildDiscarder(logRotator(numToKeepStr:'10'))
   }

   stages {      
      stage('Development Tests') {
         when {
            beforeAgent true
            branch 'development'
         }
         steps {
            echo "Run the development tests!"
         }
      }
   }
}
   
