 node(label: 'AIG_FF') {
      def mvnHome
        stage('Build') { // for display purposes
   bat label: '', script: '''C:
cd "C:\\Users\\dmurugad\\Downloads\\Katalon_Studio_Windows_64-6.3.3"
katalon -noSplash  -runMode=console -projectPath="C:\\Users\\dmurugad\\Downloads\\POC\\POC\\POC.prj" -retry=0 -testSuitePath="Test Suites/POC_Suite" -executionProfile="default" -browserType="Chrome"'''
}
    
}

 node {
  parallel {
      def mvnHome
        stage('Test') { // for display purposes
   bat label: '', script: '''C:
cd "C:\\Users\\dmurugad\\Downloads\\Katalon_Studio_Windows_64-6.3.3"
katalon -noSplash  -runMode=console -projectPath="C:\\Users\\dmurugad\\Downloads\\POC\\POC\\POC.prj" -retry=0 -testSuitePath="Test Suites/POC_Suite" -executionProfile="default" -browserType="Firefox"''' 
 }
  }
}
