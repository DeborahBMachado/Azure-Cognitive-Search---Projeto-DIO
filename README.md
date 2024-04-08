# Azure-Cognitive-Search: Projeto-DIO

Azure Cognitive Search ou Azure AI Search é um serviço que oferece recuperação de informações segura em escala sobre conteúdo de propriedade do usuário em aplicativos de busca tradicionais e conversacionais que tem funcionalidades como motor de busca, síntaxe de consultas avançadas, formatos de documentos em JSON, integração direto com outros serviços da plataforma e entre outros.

# Criando o ambiente para desenvolvimento

1. Criar os recursos AI Search, o Azure AI Services e o Storage Account

# Criando o AI Search

1. No portal do azure vá em "criar um recurso", ir nas categorias do AI + Machine Learning e pesquisar por "AI Search" e clicar para criar o recurso.
2. Ao criar um serviço de pesquisa (search service), precisaremos escolher seu grupo de recurso, o nome e o local (usar East US) e escolher o tier de preço para Básico ou Basic (clicando em Change Princing Tier e selecionando a opção Basic).

# Criando o AI Service

1. Ainda no portal do Azure, vá em "criar recurso", ir na categoria do AI + Machine Learning e clicar em criar ou create no Azure AI Services
2. Para criar o recurso Azure AI Service deve fazer o mesmo processo de criação do AI Search, acrescentando um check na caixa de seleção "By checking this box I acknowledge that I have read and understood all the terms" depois é só clicar em Review + Create"
3. Obs: É primordial que a localização do Azure AI Services seja a mesma da AI Search, caso contrário mais para frente na hora que você for entrelaçar as duas não irá aparecer na seleção

# Criando o Storage Account

1. No portal do Azure escreva na barra de pesquisa "Storage" e clique em "storage accounts"
2. No storage account clique em "create" e configure sua "Storage Account"
3. Insira o "Resource group", storage account name (ele deve ser unico), a localização (usar East US), a perfomance deve ser "Standard" e a Redundancy deve ser "LRS". Depois clique em "Review + Create"
4. Após a criado, clique em go to resource ou ir para o recurso
5. Na aba settings, vá para configurations/configrações. Você perceberá que o "Allow Blob anonymus access" estará desativado. Ative-o, pois é algo necessário nessa lab para passar o dados ao storage account
6. Entrando no Container criado, clique em upload e passe os arquivos que estão dentro desse link aqui: https://aka.ms/mslearn-coffee-reviews

# Desenvolvendo o AI Search
1. Concluindo os requisitos anteriores, vá para o recurso seu criado do AI Search e clique em Import Data e selecione o "Azure Blob Storage"
2. Após selecionar crie essa importação de data com está lá, e ao selecionar o Connection String, clique em Choose an existing Storage
3. Entrando lá, passe para o seu container criado até onde está armazenado os 9 arquivos criados anteriormente e selecione
4. Adicione os outros dados como está abaixo e vá para o Next
5. Indo ao subtópico Attach AI Services, você deve selecionar o recurso do AI Services que você criou de acordo com as notas e avisos informados anteriormente
6. Copie os dados
7. No próximo subtópico, irá aparecer um erro no Storage account connection string. Para resolver, faça esse passo a passo (clique no link azul abaixo desse texto)
8. Selecione como estiver abaixo e finalize clicando no Next
9. Por último, clique em create an indexer e configure com o name e clique em submit
10. Caso deseja ver o resultado, volta para tela inicial do seu AI Search e procure pelo Search Explorer e teste a pesquisa pela lupa com esse texto:  search=locations:'Chicago'  e cliqe em Submit/enviar

