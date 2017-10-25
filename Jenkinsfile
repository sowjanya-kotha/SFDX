#!groovy
import groovy.json.JsonSlurperClassic
node {

    def BUILD_NUMBER=env.BUILD_NUMBER
	def SFDC_USERNAME = env.SFDC_USERNAME
	
	//def toolbelt = tool 'toolbelt'
	
	stage('checkout source') {
        // when running in multi-branch job, one must issue this command
        checkout scm
    }
    
    stage('Run Provar test cases') {
    	println(SFDC_USERNAME)
    	rmsg = bat returnStdout: true, script: "ant -f ANT/build.xml -DSFDC_USERNAME_SO=${SFDC_USERNAME}"
        println(rmsg)
    }
}
