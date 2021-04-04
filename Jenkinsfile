
    node {
      def var1 = "shoaib"
      def arg = ["Groovy","Java","Python","nodeJS"]
      def tfHome = tool name: 'terraform_12_21'
      env.PATH = "${tfHome}:${env.PATH}"
      env.PATH = "${env.PATH}:/usr/local/bin"
      
      stage("Install Packer"){
          sh 'whoami'
          sh 'pwd'
          sh 'curl -o packer.zip https://releases.hashicorp.com/packer/1.4.0/packer_1.4.0_linux_amd64.zip && unzip -o packer.zip'
          sh 'ls -lrt'
      }
      
      if (var1=="shoaib"){
          stage("Check Version"){
              sh "./packer --version"
          }
      }
      
      stage("Checkout"){
           checkout scm
      }
      stage("Fouth Stage"){
          
          #sh './packer build -color=true packer.json'
          sh 'pwd;ls -lrt'
          
      }
    }
