pipeline {
    agent any

    stages {
        stage("Permission") {
            steps {
                echo "🔑 Set execute permission for gradlew"
                sh 'chmod +x ./Calculator/gradlew'
            }
        }
        stage("Compile") {
            steps {
                echo "🛠️ Compiling source code..."
                sh './Calculator/gradlew -p Calculator compileJava'
            }
        }
        stage("Build") {
            steps {
                echo "🏗️ Building project..."
                sh './Calculator/gradlew -p Calculator build'
            }
        }
        stage("Unit test") {
            steps {
                echo "🧪 Running unit tests..."
                sh './Calculator/gradlew -p Calculator test'
            }
        }
    }
}

