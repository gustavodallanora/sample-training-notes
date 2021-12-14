
# Tutorial Blockchain - VS Code, Windows, Javascript

O objetivo deste tutorial é dar os passos iniciais na preparação do ambiente e no desenvolvimento de Smart Contracts.

O foco do tutorial é a plataforma Windows, a IDE VS Code e a linguagem Javascript/Typescript.

Para aprofundar no tema, faça também os tutoriais que disponibilizados direto no VS Code pela extensão que instalaremos.

*Conteúdo Estes passos são baseados nesta documentação da [extensão de desenvolvimento Blockchain da IBM][1].*

---
## Pré-requisitos

### Instalações

Antes de começar, certifique-se de possuir instalado:

1. VS Code versão 1.40 ou superior. [Download](https://code.visualstudio.com/)
1. Docker versão v17.06.2-ce ou superior. [Download](https://www.docker.com/get-started)
1. Node 12.15.0 ou superior e npm v6.x ou superior. [Download](https://nodejs.org/en/download/)
1. Build Tools para C++ [Docs](https://github.com/felixrieseberg/windows-build-tools#windows-build-tools)
    * Rodar no powershell como administrador: ```npm install --global windows-build-tools```
1. OpenSSL v1.0.2 ou superior [Oficial](https://www.openssl.org/community/binaries.html) ou Alternativa: [Usar openssl que vem com o git](https://git-scm.com/downloads)

### Configurações

Colocar na variável de ambiente PATH os caminhos do Python e do OpenSSL, ex:
```
PATH=%PATH%;C:\Program Files\Git\usr\bin;C:\Users\gustavo\.windows-build-tools\python27\
```

Configurar variável PYTHON com o local do executável, ex:
```
PYTHON="C:\Users\gustavo\.windows-build-tools\python27\python.exe"
```
---
## Instalar a extensão

Depois de confirmados os pré-requisitos, é possível instalar a extensão.

Para isso, ir até o Market place de extensões do VS Code e buscar por: *IBM Blockchain Platform*

![image](./media/ex-install.png)

Concluída a instalação, reinicie o VS Code.

Depois de instalada a extensão será adicionado um novo ícone na barra lateral do VS Code, ao clicar neste ícone você terá acesso ao painel com as ferramentas de apoio ao desenvolvimento.

![image](./media/ex-pane.png)

Também ficará disponível um ícone quadrado no canto superior direito do editor do VS Code:

![image](./media/editor-square-icon.png)

Clicando neste ícone é apresentada a página inicial dos recursos da plataforma blockchain IBM, em especial, o link para os tutoriais que podem ser seguidos dentro do próprio VS Code.

![image](./media/ex-home.png)

:tada: Parabéns! Seu ambiente está pronto para começar!

---
## Trabalhando com Smart Contracts

Neste tópico veremos algumas operações básicas para trabalhar com Smart Contracts.

Você terá uma noção de como criar um Smart Contract, executá-lo e visualizar os resultados.

Nos tutoriais que ficam disponíveis na página inicial, vista acima, estas operações são trabalhadas com mais profundidade, então, não deixe de continuar aprofundando os seus conhecimentos.

### Conhecendo o nosso ativo

Por fins didáticos, vamos chamar o nosso ativo de ```bilhete```, como um bilhete de loteria ou de rifa.

Normalmente a definição dos ativos segue um processo criterioso, levando em consideração vários aspectos. Porém, para simplificar e facilitar ao máximo esse contato com Blockchain, vamos chamar de ```bilhete```.

Assim, sempre que a palavra ```bilhete``` aparecer, trata-se do nosso ativo digital. :wink:

### Criação do Smart Contract

Crie uma pasta no seu sistema de arquivos para colocar os fontes do Smart Contract, como sugestão, chame-a de ```bilhete-smart-contract```.

Na barra lateral da extensão, vá ao painel ```Smart Contracts``` e clique no ícone ```...```, para abrir o menu de opções e clique em ```Create New Project```

![image](./media/create-project.png)

No modal apresentado, escolha a opção ```Default Contract``` (depois, busque nos tutoriais para entender a diferença entre cada uma das opções):

![image](./media/contract-type.png)

Em seguida, escolha a linguagem que pode ser a de sua preferência, no exemplo seguiremos com ```JavaScript```:

![image](./media/lang.png)

Por fim, o nome do ativo, ou seja, ```Bilhete```. 

![image](./media/asset.png)

Agora selecione a pasta que você criou no início deste tópico, o nome sugerido foi ```bilhete-smart-contract```.

Então, quando solicitado, a opção ```Add to workspace```.

![image](./media/how-to-open.png)

Estes passos resultarão na geração de alguns arquivos na pasta ```bilhete-smart-contract```, bem como na adição desta pasta no workspace do VS Code, com a seguinte estrutura:

![image](./media/project-folder.png)

É isso aí! O ```bilhete-contract.js``` é o nosso Smart Contract!

### Empacotamento do Smart Contract

O próximo passo é criar um pacote com o Smart Contract, para que depois seja possível implantá-lo na Blockchain.

Para isso, volte na barra lateral da extensão, vá ao painel ```Smart Contracts``` e clique no ícone ```...```, para abrir o menu de opções e clique em ```Package Open Project```

![image](./media/package-project.png)

Selecione o projeto ```bilhete-smart-contract``` e a opção ```tar.gz```.

![image](./media/package-project-format.png)

Concluído o empacotamento, agora é mostrado o pacote do nosso Smart Contract no painel ```Smart Contracts```, observe que a versão do pacote é a mesma da indicada no arquivo ```package.json```.

![image](./media/packaged-smart-contract.png)

### Implantando o Smart Contract

Para este passo, você precisa confirmar que o Docker esteja rodando. Normalmente, isso pode ser feito observando o ícone do Docker na barra de ferramentas.

Com o Docker em execução, vá na barra lateral da extensão, e ao painel ```Fabric Environments``` e clique em ```1 Org Local Fabric``` para iniciar o conteiner.

![image](./media/packaged-smart-contract.png)

Aguarde alguns instantes, você pode acompanhar o progresso na aba ```Ouput``` do VS Code, o tempo pode variar conforme o desempenho do computador e a velocidade da internet, uma vez que a imagem do conteiner é obtida on line.

Concluída a operação, você verá na aba ```Ouput``` do VS Code um log similar a:
```bash
[INFO] f230bddb739c: Pull complete
[INFO] e8c6b504d6e3: Pull complete
[INFO] Digest: sha256:a0874af85d3facff63f84be23f7a799d615f61ad1d3fb586ac4402d3af8f27cf
[INFO] Status: Downloaded newer image for ibmcom/ibp-microfab:0.0.11
[INFO] ca7ba04e2756adae5ef003f3c7f07c3005c5e1a3e9cf2f421b15acd283cd1920
[INFO] C:\Users\gustavo\.fabric-vscode\v2\environments\1 Org Local Fabric>exit /b 0 
[SUCCESS] Connected to 1 Org Local Fabric
```

Indicando que a operação foi bem sucedida.

Além disso, agora será possível visualizar outros componentes da solução Blockchain na barra lateral da extensão: 

![image](./media/components-tab.png)

Agora, na barra lateral da extensão, dentro do painel ```Fabric Environments```, abra a opção ```mychannel``` e clique em ```Deploy smart contract```:

![image](./media/deploy-smart-contract.png)

No passo 1, selecione o pacote que criamos ``` ```, clique em ```Next``` e depois clique em ```Deploy```.

![image](./media/do-deploy.png)

---
## Referências

[1]: https://cloud.ibm.com/docs/blockchain-sw-252?topic=blockchain-sw-252-develop-vscode
