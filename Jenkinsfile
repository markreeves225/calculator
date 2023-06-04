pipeline {
    agent any
    triggers {

     	 pollSCM('* * * * *')

    }
    stages {
        stage("Compile") {
            steps {
                sh """
                ls
                pwd
                PATH=/usr/lib/jvm/java-17-openjdk-amd64/bin:\$PATH
                export PATH
                export JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64
                java -version
                echo \$PATH
                ./gradlew build
                """
            }
        }
    }
}

