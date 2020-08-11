# Exemplo CI/CD ![Badge](https://img.shields.io/badge/Status-Conclu%C3%ADdo-green)

Exemplo de utilização de CI/CD utilizando Jenkins / AWS / Docker

## <img src="https://img.icons8.com/ios-filled/20/000000/browser-window.png"/> Página

<p align="center">
  <img src="https://github.com/cicerorod/aws-jenkins/blob/master/images/Tela.PNG">
</p>

## ![](https://img.icons8.com/metro/20/000000/run-command.png) Clone

Clonar via prompt de comando o projeto em uma pasta de sua preferência: `git clone https://github.com/cicerorod/aws-jenkins.git`


## ![](https://img.icons8.com/metro/20/000000/run-command.png) Execução

### 1 - Instalação de Docker em servidores Ubuntu - AWS

Referência: https://docs.docker.com/install/linux/docker-ce/ubuntu/

```
$sudo apt-get remove docker docker-engine docker.io containerd runc
$sudo apt-get update
$sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common
$curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
$ sudo apt-key fingerprint 0EBFCD88
$sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
$ sudo apt-get update
$ sudo apt-get install docker-ce docker-ce-cli containerd.io
```
### 2 - Instalação do Java no Servidor Ubuntu – AWS

```
$ cd 
$ pwd 
$ sudo apt install openjdk-8-jre-headless 
```
### 3 - Instalação e Inicialização do Jenkins no Servidor Ubuntu – AWS

### 3.1 - Instalação

-  O comando será executado na pasta tools
-  O Jenkins utilizado foi (Generic Java pachage (.war)) do site https://www.jenkins.io/download/ e deve ser informado no comando wget abaixo
-  Comando deve ser executado na pasta raiz do ubuntu

```
$ cd 
$ pwd
$ ls -ltr
$ mkdir tools
$ cd /tools
$ wget http://mirrors.jenkins.io/war-stable/latest/jenkins.war
$ ls -ltr
```
### 3.2 - Inicialização

- Executar o comando para pegar as informações 'Initial password' de usuário. O comando retorna 'Initial password' (3540e56cd6cd4658b4de2dbf528a51ce) e pasta onde ficam as informações iniciais (/home/ubuntu/.jenkins/secrets/initialAdminPassword)

```
$ java -jar jenkins.war
```

- Executar “control + c” para finalizar o processo após a cópia do Initial password
- Certificar que o processo jenkins não está no ar

```
$ps -ef | grep java
```

- Subir o processo em Background

```
$java -jar jenkins.war & 
```

O Jenkins irá subir na porta 8080 do servidor.


### 4 - Comando para criação de um pipeline 


```
node {
   def mvnHome
   stage('Passo 01  - Preparação') {      
      // Sincronizar e fazer o Get do código do GitHub
      git 'https://github.com/XXXXXXX'
     
   }
   stage('Passo 02 - Docker Build') {
      // Cria a imagem docker contida no arquivo Dockerfile deste repositório
      sh "sudo docker build -t myapp ."
      
   }
   stage('Passo 03 - Parando a aplicação') { 
      // 1 Executa um container "Hello-Word" 
      // 2 Para todos os container
      // 3 exclui todos os containers da máquina
      sh label: '', script: 'sudo docker run hello-world;sudo docker stop $(sudo docker ps -a -q); sudo docker container prune -f'
      
   }
   stage('Realizando o Deploy'){
     // Executa o container e inicia o site na porta 8082 
     sh "sudo docker run --name meusite -p 8082:80 -d myapp"  
   }
}
```
- Configuração do Segurity Group AWS:

<p align="center">
  <img src="https://github.com/cicerorod/aws-jenkins/blob/master/images/SecurityGroups.PNG">
  
</p>

## ![](https://img.icons8.com/ios-filled/20/000000/hammer.png) Recursos utilizados:

- **[AWS](https://aws.amazon.com/pt/console/)**
- **[Docker](https://www.npmjs.com/package/axios)**
- **[Jenkis](https://www.npmjs.com/package/react-countup)**



## AMI de Ubuntu utilizada na AWS

+ [Ubuntu Server 20.04 LTS (HVM), SSD Volume Type](ami-01237fce26136c8cc)


## ![](https://img.icons8.com/ios-glyphs/20/000000/pull-request.png) Contribuições

1. Faça o _fork_ do projeto (<https://github.com/cicerorod/aws-jenkins/fork>)
2. Crie uma _branch_ para sua modificação (`git checkout -b feature/[nome]`)
3. Faça o _commit_ (`git commit -am 'Add files [nome]'`)
4. _Push_ (`git push origin feature/[nome]`)
5. Crie um novo _Pull Request_


## ![](https://img.icons8.com/ios-glyphs/22/000000/code-file.png) Desenvolvedor

<img src="https://avatars.githubusercontent.com/cicerorod" width=115>

[![](https://img.icons8.com/fluent/30/000000/github.png)](https://github.com/cicerorod)
[![](https://img.icons8.com/metro/25/000000/linkedin.png)](https://www.linkedin.com/in/c%C3%ADcero-rodrigues-89623784/)
[![](https://img.icons8.com/metro/25/000000/facebook.png)](https://www.facebook.com/cicero.rodrigues.90834)
[![](https://img.icons8.com/material-rounded/29/000000/instagram-new.png)](https://www.instagram.com/cicero_rod/)
[![](https://img.icons8.com/metro/26/000000/email.png)](mailto:cicerorod@gmail.com)

<p align="center">
  <img src="https://img.icons8.com/wired/32/000000/icons8-new-logo.png" >
  </br>
  <a href="https://icons8.com/icon/">Icons by Icons8</a>
  
</p>


<!--
[nodejs]: https://nodejs.org/
[yarn]: https://yarnpkg.com/
[repo]:https://github.com/cicerorod/igti-fullstack-mod3-react-paises
-->
