String branchName = env.BRANCH_NAME
String gitCredentials = "dmitriyt21@gmail.com/******"
String repoUrl = "https://github.com/dmitriyt21/appiumcicl.git"

node (label: 'this_pc1'){
  // Start Stages
  stage('Clone') {
      // Clones the repository from the current branch name
      bat 'if not exist git_repo mkdir git_repo'
      echo 'Deleting the output directory'
      bat '@RD /S /Q git_repo'
      echo 'Make the output directory'
      bat 'mkdir git_repo'
      echo 'Cloning the repo'
      dir('git_repo') {
           git credentialsId: 	gitCredentials, url: repoUrl
       }
      bat 'chdir git_repo'
      bat 'dir'
   }
//   stage('start selenium grid') {
            
//                  bat '''cd C:\\Users\\user\\Desktop\\katalon_dockers
//                      docker-compose up -d hub chrome firefox --force-recreate'''
           
//          }
//   stage('run katalon container') {
            
//                  bat '''cd C:\\Users\\user\\Desktop\\katalon_dockers
//                      docker-compose up katalon --force-recreate'''
            
//          }
//   stage('stop selenium grid') {
            
//                  bat '''cd C:\\Users\\user\\Desktop\\katalon_dockers
//                      docker-compose down'''
            
//          }
}