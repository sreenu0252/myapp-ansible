pipeline{
  agent any
     stages{
       stage('scm checkout'){
         step{
           git 'https://github.com/sreenu0252/myapp-ansible.git'
         }
      }
       stage('ansible-playbook'){
         step{
           ansiblePlaybook credentialsId: 'ansible', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dev.inv', playbook: 'apache.yml'
         }
      }
  }
}
