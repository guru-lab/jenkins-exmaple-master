node{
   
   stages {
        stage ('Compile Stage') {

            steps 
                {
                    def mvnHome = tool name: 'Maven', type: 'maven'
                   sh "${mvnHome}/bin/mvn compile"
                    
                }
            }
        }

        stage ('Testing Stage') {

            steps {
               def mvnHome = tool name: 'Maven', type: 'maven'
               sh "${mvnHome}/bin/mvn test"
                }
            }
        


        stage ('Deployment Stage') {
            steps {
              def mvnHome = tool name: 'Maven', type: 'maven'
              sh "${mvnHome}/bin/mvn deploy"
            }
        }
    }
