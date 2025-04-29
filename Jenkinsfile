pipeline {
  agent any

  stages {
    stage('Clonar código') {
      steps {
        git 'https://github.com/JuandiToroJT/pruebamaven.git'
      }
    }

    stage('Compilar') {
      steps {
        sh './mvnw clean package -DskipTests'
      }
    }

    stage('Ejecutar') {
      steps {
        sh 'nohup java -jar target/*.jar &'
      }
    }
  }
}
