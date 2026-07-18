# Laboratório prático "Um tour pelo Google Cloud"

## Visão Geral

O Google Cloud é um pacote de serviços de nuvem hospedado na infraestrutura do Google. No Google Cloud, você encontra APIs e serviços de vários tipos, incluindo armazenamento, computação, análise de dados, machine learning e rede, que podem ser integrado a aplicativos ou projetos de computação em nuvem, pessoais ou empresariais.

No Google Skills, você acessa todo o catálogo de laboratórios e cursos do Google Cloud. Você vai conhecer programas de aprendizado, desenvolver habilidades em nuvem sob demanda, monitorar seu progresso nas atividades e validar seu conhecimento com selos. O Qwiklabs é a plataforma onde ficam os laboratórios e cursos. Você vai encontrar o nome Qwiklabs em sua jornada de aprendizado no Google Cloud.

Neste laboratório introdutório, você vai começar a usar o Google Cloud com o [console do Cloud](https://cloud.google.com/cloud-console?hl=en), uma UI para navegador que permite acessar e gerenciar os serviços do Google Cloud. Além disso, vai identificar os principais recursos do Google Cloud e conhecer os detalhes do ambiente do laboratório.

Aqui é o lugar certo para quem é iniciante em computação em nuvem ou quer ter uma visão geral do Google Cloud e da plataforma do Qwiklabs. Leia a selção a seguir para conferir os detalhes deste laboratório e as áreas em que você terá experiência prática.

## Objetivos

Neste laboratório, você aprenderá a fazer o seguinte: 

* Acessar o console do Cloud com credenciais específicas para explorar a plataforma do laboratório e identificar os principais recursos de um ambiente de laboratório.

* Conhecer vários projetos do Google Cloud e identificar equívocos comuns relacionados a eles.

* Usar o menu de navegação do console do Google Cloud para identificar os tipos de serviços.

* Gerenciar papéis básicos e uso do serviço Cloud IAM para verificar ações disponíveis para usuários específicos.

* Examinar os principais recursos da biblioteca de APIs.

## Pré-requisitos

Este laboratório é de *nível introdutório*. Ele é o primeiro que você precisa concluir para se familiarizar com o Google Cloud. Se você já tem experiência com o console do Cloud, faça um destes laboratórios: 

* [Como começar a usar o Cloud Shell e o gcloud](https://google.qwiklabs.com/catalog_lab/320)

* [Criar uma máquina virtual](https://www.skills.google/focuses/3563?parent=catalog)

# Noções básicas do laboratório

## Recursos e componentes

Seja qual for o tópico ou nível de especialização, todos os laboratórios têm a mesma interface. O laboratório que você está fazendo deve ser parecido com este: 

![](https://cdn.qwiklabs.com/Gx5QWak6EsvW0PQURmiMyf10sLtl2AT%2BUSrD04WuCzY%3D)

**Observação:** você não está no laboratório a "Como criar uma máquina virtual" que aparece na imagem. Esse é um exemplo para mostrar elementos comuns em qualquer laboratório.

Leia as definições dos componentes do laboratório a seguir e localize cada um deles na interface.

**Botão "Começar laboratório"**

Ao clicar nesse botão, você cria uma ambiente temporário do Google Cloud, com todos os serviços e credenciais necessários ativados, para poder praticar com o material do laboratório. Essa ação também inicia um timer de contagem regressiva.

**Crédito**

O preço de um laboratório. *Geralmente*, 1 crédito equivale a 1 dólar americano. Quanto mais créditos você compra, maior é o desconto. Alguns laboratórios de nível introdutório (como este) não têm custo algum. Os laboratórios especializados custam mais, porque envolvem tarefas de computação mais complexas e que exigem mais recursos do Google Cloud.

**Tempo**

Especifica o tempo que você tem para concluir um laboratório. Quando você clica no botão "Começar laboratório", o timer inicia a contagem regressiva até atinfir 00:00:00. Nesse momento, seu ambiente e os recursos temporários do Google Cloud são excluídos. O tempo é suficiente para concluir um laboratório, mas evite realizar outras tarefas enquanto ele estiver em execução, porque você pode perder todo o trabalho.

**Pontuação**

Muitos laboratórios incluem uma pontuação. Esse recurso é chamado de "rastreamento de atividades" e confirma que você concluiu as etapas especificadas em um laboratório. Você precisa concluir todas as etapas *na ordem* em que aparecem para ter aprovação em um laboratório com restreamento de atividades. Só depois disso você poderá receber o crédito pela conclusão.

## Como pagar por um laboratório

Alguns laboratórios não têm custo financeiro, mas outros são pagos. Quando você clica no botão "Começar laboratório", uma caixa de diálogo mostra a opção de iniciar o laboratório com um código de acesso ou créditos. Se você não tiver nenhum dos dois, clique em **Comprar créditos** e siga as instruções.

## Onde encontrar as instruções

Esta guia do navegador contém as instruções do laboratório. Quando você começa um laboratório, a interface do usuárioo do console do Google Cloud abre uma nova guia do navegador. Talvez você precise alternar entre as duas guias para ler as instruções e realizar as tarefas. Dependendo da configuração do seu computador você também pode exibir cada uma das guias em monitores separados.

# Tarefa 2: acessar projetos no console do Cloud

Os projetos do Google Cloud são explicados na seção de conteúdos do painel de detalhes do laboratório. Veja a definição mais uma vez:

Um projeto do Google Cloud é uma entidade que organiza os recursos do Google Cloud. Ele geralmente contém recursos e serviços, por exemplo: um pool de máquinas virtuais, um conjunto de bancos de dados e uma rede que conecta isso tudo. Os projetos também contêm configurações e permissões que especificam regras de segurança e quem tem acesso a quais recursos.

No canto superior esquerdo do painel central, está o cartão rotulado como Informações do projeto.

![](https://cdn.qwiklabs.com/kaHKc2t7OyP7YUPOj4Eqw0nuUXQvt0iUypsuaeqkzKw%3D)

Seu projeto tem um nome, número e ID. Esses identificadores são usados com frequência na interação com os serviços do Google Cloud. Você está trabalhando em um projeto para ter experiência com um serviço ou recurso específico do Google Cloud.

## Ver todos os projetos

Neste laboratório, você tem acesso a mais de um projeto do Google Cloud. Em alguns laboratórios, você pode receber mais de um projeto para concluir as tarefas atribuídas.

1. Na barra de título do console do Google Cloud, ao lado do nome do projeto, clique no menu suspenso.

2. Na caixa de diálogo **Selecionar um projeto**, clique em **Todos**. A lista exibida incluirá o projeto "Qwiklabs Resources".

**Observação: não mude para o projeto "Qwiklabs Resources" agora. Mas você pode precisar usá-lo em outros laboratórios.**

É comum que grandes empresas ou usuários experientes tenham dezenas ou milhares de projetos do Google Cloud. As organizações usam o Google Cloud de maneiras diferentes. Por isso, os projetos são um bom método para organizar os serviços de computação em nuvem (por equipe ou produto, por exemplo).

O projeto "Qwiklabs Resources" contém arquivos, conjuntos de dados e imagens de máquina para determinados laboratórios e pode ser acessado de todos os ambientes de laboratório do Google Cloud. Ele é compartilhado (somente leitura) com todos os usuários estudantes, ou seja, não pode ser excluído ou modificado.

Você está trabalhando em um projeto temporário do Google Cloud. Isso significa que o projeto e o conteúdo dele serão excluídos quando o laboratório terminar. Ao iniciar um novo laboratório, você recebe acesso a um ou mais projetos novos do Google Cloud. Realize todas as etapas do laboratório nesses projetos, não no projeto "Qwiklabs Resources".

## Menu de navegação e serviços

A barra de títulos do console do Google Cloud também conta com o **menu de navegação**.

![](https://cdn.qwiklabs.com/nUxFb6oRFr435O3t6V7WYJAjeDFcrFb16G9wHWp5BzU%3D)

Ao clicar no ícone, você abre ou oculta o *menu de navegação*, que oferece acesso rápido aos principais serviços do Google Cloud.

1. Se o menu não abrir, clique no **menu de navegação**.

2. Clique em **Conferir todos os produtos** e navegue pelas categorias de ferramentas e serviços.

Consulte a [página de visão geral dos produtos do Google Cloud](https://cloud.google.com/products?hl=pt-BR#top_of_page) para conferir a documentação de cada uma dessas categorias com mais detalhes.

# Tarefa 3: analisar e modificar papéis e permissões

Além dos serviços de computação em nuvem, o Google Cloud inclui permissões e papéis para definir quem tem acesso a cada recurso. Use o serviço [Cloud Identity and Access Management (Cloud IAM)](https://cloud.google.com/products/iam?hl=en) para inspecionar e modificar esses papéis e permissões.

## Ver seus papéis e permissões

1. No **menu de navegação**, clique em **IAM e Admin** > IAM. A página que contém uma lista de usuários, permissões e papéis concedidos a contas específicas é aberta.

2. Encontre o nome de usuário "@qwiklabs" que você usou para fazer login no laboratório.

![](https://cdn.qwiklabs.com/VpeV7knPXEDf39QBcfOJuAZpDB7zPgjzMSFmmCy2avk%3D)

A coluna Principal mostra o e-mail estudante-xx-xxxxxx@qwiklabs.net. Neste laboratório, o endereço de e-mail principal corresponde ao nome de usuário usado no login: student-02-39136afda682@qwiklabs.net. A coluna Nome mostra estudante XXXXXXXX, e a coluna Papel mostra Editor, que é um dos três papéis básicos oferecidos pelo Google Cloud.

Os papéis básicos definem permissões para envolvidos no projeto e, a menos que especificado de outra maneira, controlam o acesso e o gerenciamento de todos os serviços do Google Cloud. A tabela a seguir mostra as definições da documentação de papéis sobre as permissões de leitor, editor e proprietário.

![]()

Como editor, você pode criar, modificar e excluir recursos do Google Cloud. No entanto, não é possível adicionar ou excluir membros de projetos do Google Cloud.

## Conceder um papel do IAM

Nesta seção, você vai fazer uma atualização simples do IAM para conceder ao principal o papel de `leitor` no projeto.

1. No **menu de navegação**, clique em **IAM e Admin** > **IAM**.

2. Clique em **Conceder acesso**.

3. Na seção **Adicionar principais**, insira um identificador `User 2` para o principal.

4. No menu suspenso **Selecionar um papel** na seção **Atribuir papéis**, pesquise **Leitor** e clique em **Leitor**.

5. Clique em **Salvar**.

6. Verifique se o principal e o papel correspondente estão listados na página do IAM.

Você concedeu um papel do IAM a uma segunda conta de estudante.

**Observação:** agora você encontrará um recurso chamado Monitoramento de Atividade que avalia a conclusão de uma tarefa. Conforme você completa as tarefas e tem sua evolução avaliada com o teste "**Verificar meu progresso**", sua pontuação aumenta na caixa do canto superior direito. Essa pontuação determina a conclusão do laboratório para você receber selos e credenciais. Ela também contribui para a posição na tabela de classificação em jogos do laboratório.

Neste caso, o Monitoramento de Atividade é fornecido para verificar se você concedeu o papel do IAM.

# Tarefa 4: ativar APIs e serviços

As APIs são uma parte importante do Google Cloud. Assim como os serviços, as mais de 200 APIs de diversas áreas, como administração de empresas e machine learning, são facilmente integradas aos projetos e aplicativos do Google Cloud.

APIs são *interfaces de programação de aplicativo* que você pode chamar diretamente ou nas bibliotecas de cliente. As APIs do Cloud usam os princípios de criação orientados a recursos, conforme descrito no [Guia de design de APIs](https://docs.cloud.google.com/apis/design).

Quando o laboratório fornece um novo projeto do Google Cloud para uma instância, ele ativa muitas APIs automaticamente para você começar a trabalhar nas tarefas dele o mais rápido possível. Você vai precisar ativar algumas APIs por conta própria quando criar seus projetos do Google Cloud fora do ambiente do laboratório.

A maioria das APIs do Cloud apresenta informações detalhadas sobre o uso de determinada API no seu projeto, inclusive níveis de tráfego, taxas de erros e até latências. Assim você identifica rapidamente os problemas com os aplicativos que usam os serviços do Google.

1. No **menu de navegação**, clique em **APIs e serviços** > **Biblioteca**. No cabeçalho **Categoria**, do painel à esquerda, são mostradas as diferentes categorias disponíveis.

2. Na barra de pesquisa de APIs, digite **Dialogflow** e clique em **API Dialogflow**. A página com a descrição da API Dialogflow será aberta.

Com a API Dialogflow, você pode criar aplicativos de conversação avançados (por exemplo, para o Google Assistente) sem precisar entender os esquemas subjacentes de machine learning e de linguagem natural.

3. Selecione **Ativar**.

Clique no botão "Voltar" do navegador para verificar se a API está ativada.

![](https://cdn.qwiklabs.com/eTgnbsNvLaqrex7qumvUuzQEc114GwncM%2FV8xL4j594%3D)

5. Clique em **Testar esta API**. Uma nova guia do navegador vai mostrar a documentação da API Dialogflow. Leia as informações e feche a guia quando terminar.

6. Para retornar à página principal do console do Cloud, no **Menu de navegação**, clique em **Visão geral do Cloud**.

Quer saber mais sobre APIs? Consulte o [Diretório de APIs Explorer do Google](https://developers.google.com/apis-explorer?hl=pt-br#p/). O laboratório [APIs Explorer: Qwik Start](https://www.skills.google/focuses/2457?parent=catalog) também traz experiência prática com a ferramenta, usando exemplos simples, como níveis de tráfego, taxas de erro e até latências. Isso ajuda você a fazer uma triagem rápida dos problemas com aplicativos que usam os serviços do Google.



