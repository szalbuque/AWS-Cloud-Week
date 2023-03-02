# AWS-Cloud-Week Repositório para o projeto
Três dias práticos para construir uma aplicação de chat serverless na nuvem AWS.
## Setup
### Sistema operacional: Windows 11 Pro
* Hardware: 
  * Processador: 11th Gen Intel(R) Core(TM) i3-1115G4 @ 3.00GHz   3.00 GHz
  * Ram: 8Gb
### Instalação do Node.js
* Versão utilizada: 17.7.1
* Fonte: https://nodejs.org/en/blog/release/v17.7.1/
* Arquivo:  https://nodejs.org/dist/v17.7.1/node-v17.7.1-x64.msi
* Para testar se foi instalado:
    > node -v<br>
    > v17.7.1
 ### Outros softwares e configurações:
 * Git (instalado, versão 2.37.0.windows.1);
 * Conta criada no GitHub;
 * Visual Studio Code (instalado, versão 1.75.1);
 * Configurar a integração do VSCode com o GitHub;
### AWS
* Usuário criado: silvia_cloud_week;
* Com acesso ao AWS Management Console;
* Marcado: "I want to create an IAM user";
* Senha gerada automaticamente;
* Usuário precisa criar nova senha no próximo login;
* Usuário criado sem nenhuma permissão;
* Importante! Fazer o download do arquivo csv (esta é a única chance!):
  
![](imagens/awsusercreated.png)

* Ao acessar com o endereço fornecido nesta tela (Console Sign-in URL), aparece uma tela para o login deste usuário:

![](imagens/IAMuserlogin.png)

* Conforme eu havia configurado, o console solicita a troca da senha no primeiro acesso:

![](imagens/Changepasswd.png)

* Porém, como não dei nenhuma permissão a esse usuário, não conseguirei acessar os recursos. 
* A tela abaixo mostra os avisos decorrentes da falta de permissão:

![](imagens/permissionError.png)

* Para corrigir, preciso entrar como root e adicionar permissões. Mesmo que o usuário silvia_cloud_week esteja logado, as permissões serão aplicadas imediatamente, bastando dar um refresh na página do console.

![](imagens/afterPermissionEC2full.png)

* O ideal é criar grupos e adicionar as permissões aos grupos. Daí, todos os usuários de um dado grupo terão as mesmas permissões de acesso. A aplicação das permissões também é imediata nesse caso.

<h4><b>Backend Serverless AWS</b></h4>

* Neste exercício são usados:
  * AWS Lambda:
    * Executa código em resposta a eventos;
    * Exemplos: chamada de API, upload de arquivo, atualização de BD;
    * Componentes principais: <b>eventos</b> (gatilho para execução), <b>funções</b> (código a executar), <b>recursos</b> (componentes usados pela função);
  * Amazon API Gateway

## A aplicação:
* Repositório: https://github.com/cassiano-dio/chatgpt-nodejs-api
* Neste exercício, o código será enviado para o AWS Lambda por um arquivo zip. Mas é possível integrar com um pipeline CI/CD, como o do GitHub, por exemplo. Também há serviços de CI/CD na AWS.
* 

