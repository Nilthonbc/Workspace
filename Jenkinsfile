pipeline {
        agent any

        stages {
                tage('Preparar entorno') {
            steps {
                echo "Creando entorno virtual..."
                bat '"C:\Users\nilto\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Python 3.13" -m venv venv'
                bat 'venv\\Scripts\\activate && pip install -r requirements.txt'
            }
        }

        stage('Ejecutar script') {
            steps {
            echo "Ejecutando script principal..."
            bat 'venv\\Scripts\\activate && python prueba.py'
            }
        }
    }

    post {
        success { echo "✅ Pipeline completado con éxito" }
        failure { echo "❌ Error en alguna etapa del pipeline" }
        }
}
