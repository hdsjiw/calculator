pipeline {
    agent any

    stages {
        stage("Permission") {
            steps {
                echo "🔑 Set execute permission for gradlew"
                sh 'chmod +x ./gradlew'
            }
        }
        stage("Compile") {
            steps {
                echo "🛠️ Compiling source code..."
                sh './gradlew compileJava'
            }
        }
        stage("Build") {
            steps {
                echo "🏗️ Building project..."
                sh './gradlew build'
            }
        }
        stage("Unit test") {
            steps {
                echo "🧪 Running unit tests..."
                sh './gradlew test'
            }
        }
    }
}
