node('BuildServer'){

    checkout scm
   
    stage("Provision Load and Run"){   
            sh "./exec-jmeter.sh 3"
            perfReport compareBuildPrevious: true, percentiles: '0,50,90,100', sourceDataFiles: '**/results/**/results'
        
        }        
}
