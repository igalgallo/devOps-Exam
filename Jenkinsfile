node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t 6686:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'igalgallo' -p 'tx@Molsal75' "
sh "docker tag 6686:latest igalgallo/6686:latest"
sh "docker push igalgallo/6686:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}
