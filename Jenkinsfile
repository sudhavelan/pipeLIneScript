def report = 'Failed in Step: '
def reporttxt
pipeline {
    //agent any
	agent { label "localhost" }
    stages {
        stage("setupenv") {
            steps {
				script {
					reporttxt = report + "setupenv";
				}
				checkout([$class: 'GitSCM', branches: [[name: '*/develop']], doGenerateSubmoduleConfigurations: false, extensions: [[$class: 'SubmoduleOption', disableSubmodules: true, parentCredentials: false, recursiveSubmodules: true, reference: '', trackingSubmodules: false]], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'AIM_GHES', url: 'https://github.softwareag.com/AIM/api-portal.git']]])
			}
        }        
	}    
}
