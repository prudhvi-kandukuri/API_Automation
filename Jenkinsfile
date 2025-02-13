pipeline {
    agent any

    tools { 
        nodejs "nodejsLocal" 
    }

    stages {  // 🔹 Added "stages" block to wrap all "stage" blocks
        stage('Postman CLI Login') {
            steps {
                bat 'postman login --with-api-key PMAK-67aaf2d5219b200001e9fdfd-8922d11cd33281cbde3bbdb71c8b7e80f3'
            }
        }

        stage('Running collection') {
            steps {
                bat 'postman collection run "40848720-36fa518b-1d25-4a5d-a4db-e4542626c7f6" -d "C:/Users/Prudhvi.Kandukuri/OneDrive - Entain Group/API Testing/video9/products_collection/products_collection/product_data.json" -g "C:/Users/Prudhvi.Kandukuri/OneDrive - Entain Group/API Testing/video9/products_collection/products_collection/workspace.postman_globals.json" -r html'
            }
        }
    }
}
