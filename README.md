# Exemplo CI/CD ![Badge](https://img.shields.io/badge/Status-Conclu%C3%ADdo-green)

Exemplo de utilização de CI/CD utilizando Jenkins / AWS / Docker

## <img src="https://img.icons8.com/ios-filled/20/000000/browser-window.png"/> Página

<p align="center">
  <img src="https://github.com/cicerorod/igti-fullstack-mod3-react-salario-frontend/blob/master/img/tela.PNG">
</p>

## ![](https://img.icons8.com/metro/20/000000/run-command.png) Clone

Clonar via prompt de comando o projeto em uma pasta de sua preferência: `git clone https://github.com/cicerorod/aws-jenkins.git`


## ![](https://img.icons8.com/metro/20/000000/run-command.png) Execução

### Instalação de Docker em servidores Ubuntu

Referência: https://docs.docker.com/install/linux/docker-ce/ubuntu/

```
$ sudo apt-get remove docker docker-engine docker.io containerd runc
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








<!-- :hammer:-->

## ![](https://img.icons8.com/ios-glyphs/20/000000/api.png) API utilizada para consumo dos dados

A aplicação necessita da API para retorno da votação. O Código pode ser baixada [aqui][backend]

## ![](https://img.icons8.com/ios-filled/20/000000/hammer.png) Recursos utilizados:

- **[ReactJS](https://reactjs.org/)**
- **[Axios](https://www.npmjs.com/package/axios)**
- **[React-countup](https://www.npmjs.com/package/react-countup)**
- **[React Dom](https://www.npmjs.com/package/react-dom)**
- **[HTML](https://www.w3schools.com/html/)**
- **[JavaScript](https://www.w3schools.com/js/)**
- **[CSS](https://www.w3schools.com/Css/)**
- **[Materialize-css](https://materializecss.com/)**
- **[ES6+](https://www.w3schools.com/Js/js_es6.asp)**
- **[Visual Studio Code](https://code.visualstudio.com/?WT.mc_id=hackingcarreira_wmc-github-gllemos)**

## ![](https://img.icons8.com/ios-glyphs/20/000000/pull-request.png) Contribuições

1. Faça o _fork_ do projeto (<https://github.com/cicerorod/igti-fullstack-mod3-react-salario-frontend/fork>)
2. Crie uma _branch_ para sua modificação (`git checkout -b feature/[nome]`)
3. Faça o _commit_ (`git commit -am 'Add files [nome]'`)
4. _Push_ (`git push origin feature/[nome]`)
5. Crie um novo _Pull Request_

## ![](https://img.icons8.com/windows/20/000000/regular-document.png) Licença

Este projeto está sob a licença do MIT. Consulte [LICENSE](https://github.com/cicerorod/igti-fullstack-mod3-react-salario-frontend/blob/master/LICENSE) para obter mais informações.

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

[backend]: https://github.com/cicerorod/igti-fullstack-mod3-react-salario-backend

<!--
[nodejs]: https://nodejs.org/
[yarn]: https://yarnpkg.com/
[repo]:https://github.com/cicerorod/igti-fullstack-mod3-react-paises
-->
