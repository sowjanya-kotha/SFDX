#!groovy
import groovy.json.JsonSlurperClassic
node {

    def BUILD_NUMBER=env.BUILD_NUMBER
	def SFDC_USERNAME = env.SFDC_USERNAME
	
	//def toolbelt = tool 'toolbelt'
	
    stage('Run Provar test cases') {
    	rmsg = bat returnStdout: true, script: "ant -f ANT/build.xml -DSFDC_USERNAME_SO=${SFDC_USERNAME}"
        println(rmsg)
    }
}
