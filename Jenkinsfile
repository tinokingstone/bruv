//jenins for angualr
//clone angular repo
//cd into repo
//run built-in tests ng test, e2e
//run backend (rest server)
//deploy actual frontend 
pipeline{
	agent any
	//tools { 
        //	maven 'Maven 3.3.9' 
        //	jdk 'jdk8' 
    	//}
	stages{
	    stage('Deploy'){
		steps{
		    sh '''
		    pwd
		    ssh groupproject@51.137.130.31 << EOF
		    rm -rf spring-petclinic-rest
		    git clone https://github.com/spring-petclinic/spring-petclinic-rest
		    cd spring-petclinic-rest
		    docker run -p 9966:9966 springcommunity/spring-petclinic-rest
		    
		//running back end maven (petclinic-rest)
		//cd ..
		//running frontend api (petclinic-angular)
		//rm -rf spring-petclinic-angular
		//git clone https://github.com/spring-petclinic/spring-petclinic-angular.git
		//cd spring-petclinic-angular
		    '''
		}
	    }
	}
}
