node {
        stage ('Compile Stage') {
                withMaven(maven : 'maven_3_6_3') {
                    sh 'mvn clean compile'
                }
        }
}
node{
        stage ('Testing Stage') {
                withMaven(maven : 'maven_3_6_3') {
                    sh 'mvn clean install'
                }
        }
}

node{
        stage ('Deployment Stage') {
                withMaven(maven : 'maven_3_6_3') {
                    sh 'mvn deploy'
                }
        }
    }
