pipeline {
    agent any
    environment {
        PATH = "${PATH}:${getTerraformPath()}"
    }
    stages {
        stage('TerraformInit') {
            steps {
                sh "terraform init"
                sh "terraform apply -auto-approve"
               #sh "terraform destroy -auto-approve"
            }
        }
    }
}

def getTerraformPath(){
    def tfHome = tool name: 'inJenkinsMyTerraform', type: 'terraform'
    return tfHome
}
