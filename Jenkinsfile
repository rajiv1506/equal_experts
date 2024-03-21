pipeline {
    agent any

    stages {
        stage('Cloning') {
            steps {
                git url:"https://github.com/rajiv1506/equal_experts.git", branch:"main"

            }
        }
        stage('Building Tag') {
            powershell 'cd equal_experts'
            def tag = buildtag()
        }


    }
}

def buildtag(){
    powershell 'git rev-parse --short HEAD'
}
