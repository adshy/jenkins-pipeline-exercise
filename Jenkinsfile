node {
    stage ('Preperation'){
        git credentialsId: '76bd5caa-ab6b-4245-a865-09e9c135f985', url: 'git@github.com:praqma-training/jenkins-pipeline-exercise.git'
        steps {
                echo 'Preparation..'
            }
    }
    stage ('Build'){
        sh'pwd'
        sh'./gradlew clean test jar'
        steps {
                echo 'Building..'
            }
    }
    stage ('Result'){
        junit '**/build/test-results/test/TEST-*.xml'
        archiveArtifacts 'build/libs/*'
        steps {
                echo 'Result..'
            }
    }
}
