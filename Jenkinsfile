
    node {
      def var1 = "shoaib"
      def arg = ["Groovy","Java","Python","nodeJS"]
      def tfHome = tool name: 'terraform_12_21'
      env.PATH = "${tfHome}:${env.PATH}"
      env.PATH = "${env.PATH}:/usr/local/bin"
      
      stage("First Stage"){
          sh 'whoami'
          sh 'pwd'
          sh 'cd /root'
          sh 'pwd'
          sh 'touch file'
          sh "echo 'this is file region'> file"
          sh 'cat file'
      }
      
      if (var1=="shoaib"){
          stage("Shoaib Stage"){
              sh "sed 's/region/eu-central-1/g' file"
          }
      }
      
      stage("Third Stage"){
          println arg[1]
          println arg.class
      }
      stage("Fouth Stage"){
          checkout scm
          sh 'aws s3 ls'
          
      }
    }
