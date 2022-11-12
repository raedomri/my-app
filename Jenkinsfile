pipeline{
    agent any
   
    stages{
        stage("git pull"){
            steps{


                git branch: 'master',
                credentialsId: '60527384-563b-4df0-85b8-10954cf21222',
                url: 'https://github.com/raedomri/my-app.git'

                }

            }
stage('Build') {
             steps{
                script{
                    sh " ansible-playbook ansible/build.yml -i ansible/inventory/host.yml"
                }
            }
        }
}
}
