node{
    stage('SCM Checkout'){
        git 'https://github.com/mahesh203/calcwebapp.git'
    }
    stage('Compile Package'){
        def mvnHome = tool name: 'M2', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    stage('Deploy to Tomcat'){ 
        sh 'cp target/*.war /opt/tomcat/webapps'
    }    
}
