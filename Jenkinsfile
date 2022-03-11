pipeline {
    agent any
    parameters {
    choice(
        name: 'myParameter',
        choices: "Option1\nOption2\nOption3",
        description: 'interesting stuff' )
    }
    stages {
        stage('Example') {
            steps {
                echo "Choice: ${params.myParameter}"
            }
       
        }
        stage('Build') {
            steps {
                
                git branch: 'main', url: 'https://github.com/vikashoo7/multi.git'
                echo 'Pulling...' + env.BRANCH_NAME
            }
       
        }
    }
}
