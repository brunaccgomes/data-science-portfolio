# Objetivo
Este projeto analisará as avaliações realizadas pelos clientes na plataforma do Google Maps referente aos restaurantes do bairro da Vila Campesina, Osasco, SP.
O objetivo desta análise é entender a dinâmica dos restaurantes do ponto de vista dos clientes através da identificação de padrões sob os comentários de avaliação de cada estabelecimento dentro do perímetro.

# Seleção
- Implementar API Google Maps Plataform via Python;
  - API Google Maps / API Places 
- Definir o perímetro do bairro Vila Campesina;
- Definir o tipo de estabelecimento como "Restaurantes" 

Extrair informações sobre estabelecimentos e avaliações do bairro Vila Campesina, Osasco, SP, usando a API do Google com Python:

**1. Ativar a API do Google Analytics:**
  - Configure o escopo e as credenciais do Google Analytics no seu script Python.
  - Use os métodos **report()** e **batchGet()** para estruturar o escopo de dados.
  - Extraia os dados necessários e faça upload para o Google Planilhas.
    
**2. Configurar o ambiente do Google API:**
  - Acesse o Google API Console com sua conta do Gmail.
  - Crie um novo projeto e selecione a API "Analytics Reporting API".
  - Defina o papel como "Proprietário" e faça o download do arquivo JSON gerado.
  - Esse arquivo será usado como chave de segurança para acessar e coletar dados no Google Analytics.
    
**3. Versão da API do Google Analytics:**
  - Use a versão 4.0 da API do Google Analytics, pois a versão 2.0 não funciona bem em ambientes locais.
  - A versão 4.0 permite a extração e consultas de dados do GA quando você tem um e-mail da API com acesso a "Leitura e Análise" dentro de uma conta do GA.
    
**4. Configurar o Python para a primeira consulta:**
  - Certifique-se de ter o Anaconda Navigator instalado.
  - Instale as bibliotecas necessárias, como BeautifulSoup e Requests.
  - Importe as bibliotecas necessárias no seu script Python.
  - Use o e-mail criado no Google API para acessar a conta do Google Analytics e fazer consultas de dados.

Lembre-se de adaptar essas etapas ao seu caso específico e explorar a documentação oficial da API do Google Analytics para obter mais detalhes sobre os endpoints e parâmetros disponíveis.
