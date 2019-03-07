node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t devOps_Exam:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'igalgallo' -p 'tx@Molsal75' "
sh "docker tag devOps_Exam:latest igalgallo/devOps_Exam:latest"
sh "docker push igalgallo/devOps_Exam:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}