node ('node1'){
    stage ('scm'){
        git 'https://github.com/akashvarma43/game-of-life.git'
    }
    stage ('build'){
        sh 'mvn package'
    }
    stage ('post build'){
        junit 'gameoflife-web/target/surefire-reports/*.xml'
        archiveArtifacts artifacts: 'gameoflife-web/target/*.war', followSymlinks: false
    }
}