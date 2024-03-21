pipeline {
    agent any

    stages {
        stage('Cloning') {
            steps {
                git url:"https://github.com/rajiv1506/equal_experts.git", branch:"main"

            }
        }
        stage('Building Tag') {
            sh 'cd equal_experts'
            def tag = buildtag()
        }


    }
}

def buildtag(){
    sh 'git rev-parse --short HEAD'
}
