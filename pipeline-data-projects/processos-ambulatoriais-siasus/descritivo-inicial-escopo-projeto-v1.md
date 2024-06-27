# Descritivo Inicial de Escopo do Projeto

## 1. Contexto
Leitura do arquivo PA - Procedimentos Ambulatoriais do SIASUS

## 2. Objetivo do Projeto
Desenvolvimento de sistema back-end que, através de interação do usuário(s) e/ou sistema(s), recebe valores de atribuição aos parâmetros de entrada, necessários no processamento que visa selecionar e disponibilizar os arquivo(s) contendo dataset(s) específicos, relacionados aos Procedimentos Ambulatoriais do SIASUS.

O back-end será utilizado em:
- Aplicação Web sob o padrão de projeto e framework Django.
- Web API que preciso pensar como seus serviços serão acessados.

## 3. Premissas do Sistema
- Ser escalável, ou seja, a estrutura é desacoplada/independente das interfaces de uso(sistemas web ou web api).
- Possuir capacidade de receber valores de entrada dos parâmetros necessários para processamento dos dados que serão fornecidos pelo usuário via diversas interface de interação,ou por processos de sistemas, legados ou não, entre outros. 
- Poderá ser incorporado como tarefa em processos automatizados/orquestrados em pipelines de dados.
- Ser desenvolvido sob algum padrão de projeto que seja performático e conveniente em relação ao seu uso e objetivo.

## 4. Especificação Técnica / Não Funcional

Desenvolver sistema back-end:
- Sistema Operacional: Windows 11
- IDE: VS Code
- Linguagem de Desenvolvimento: Python - versão 3.12
- Frameworks:
	- Django - para sistema web
	- Definir - para web api
- Banco de Dados:
  - SQL Server 2019
  - Postgresql

## 5. Especificação Funcional

O sistema back-end deve comparar o nome das colunas de um determinado dataset e sinalizar se em um determinado diretório existem arquivos com nomes correspondentes aos das colunas.
Para isso recebe os parâmetros necessários para comparar o nome das colunas de um determinado dataset e sinalizar se em um determinado diretório existem arquivos com nomes correspondentes aos das colunas, considerando as premissas citadas acima sobre a nomenclatura arquivos do diretório.

- Sobre a nomenclatura arquivos do diretório:
	- Existem arquivos que contemplam o mesmo contexto, porém direcionados para uma específica UF do Brasil. Nestes casos:
		- Possuem prefixo composto por sigla uf do Brasil, seguido por underline "_" (por exemplo, sp_micibgec.cnv, referente ao estado de São Paulo).
			- O restante do nome pode ser igual a algum nome de uma das colunas do dataset.
		- Possuem sufixo composto por underline "_" seguido por sigla uf do Brasil (por exemplo, arquivo_sp.cnv, referente ao estado de São Paulo).
			- O início do nome do arquivo pode ser igual a algum nome de uma das colunas do dataset.
	- Existem arquivos que contemplam o mesmo contexto, porém direcionados para uma específica uma das 5 regiões do Brasil. Nestes casos:
		- Possuem sufixo composto por 2 últimos caracteres representando a sigla da Região do Brasil (por exemplo, REGIACO.cnv, referente a região Centro-Oeste).
			- O início do nome do arquivo pode ser igual a algum nome de uma das colunas do dataset.
	- Os demais arquivos são considerados de uso global.

## 6. Sugestões para Desenvolvimento da Funcionalidade na Aplicação (não contemplam todo o fluxo esperado)

### 6.1. Variáveis/Parâmetros Necessário para Processamento
**Considerar as variáveis para processamento:**
- Criar e atribuir o valor para variável string que deve conter a descrição do path do diretório de origem que será consultado.
- Criar e atribuir o valor para variável string que deve conter o nome do arquivo referência (dataset) e sua extensão, arquivo este que será acessado para leitura da linha que contém o nome das colunas.
- Criar e atribuir o valor para variável string que deve conter a descrição do tipo de separador de coluna, caso o arquivo referência utilize separador de colunas.
- Criar e atribuir o valor para variável string que deve conter descrição do path de destino para cópias de arquivos.
      
### 6.2. Funcões de Processamento
**Considerar a implementação das funções para processamento**

**Função 1**
- Ler variável string que deve conter a descrição do path de diretório de consulta.
- Verificar se esse diretório existe.
	- Caso exista:
		- Ler variável string que deve conter nome do arquivo completo, ou seja, indicando a extensão também.
		- Ler variável string que deve conter o nome do tipo de separador de coluna, para o caso de verificação posterior, aonde tipo de arquivo necessite de um separador de colunas.
		- Verificar se o arquivo existe dentro do diretório informado.
			- Caso exista:
				- Acessar o arquivo que se encontra no diretório informado. 
				- Listar o nome de cada uma das colunas existentes em uma variável.

**Função 2**
- Ler variável string que deve conter path de determinado diretório.
- Ler variável string que deve o nome do tipo de extensão de arquivo.
- Verificar se esse diretório existe.
	- Caso diretório exista:
		- Acessar este diretório
		- Percorrer o diretório verificando somente arquivos e verificando a extensão de cada um:
			- Caso exista arquivo de extensão que seja igual ao informado na variável que contém o nome do tipo de extensão de arquivo:
				- Incrementar lista com o nome dos arquivos de mesma extensão.
			- Caso não exista arquivos com extensão igual ao informada na variável que contém o nome do tipo de extensão de arquivo:
				- Exibir mensagem informando que no diretório (exiber nome do diretório) não foram encontrados arquivos com a extensão (exiber nome da extensão) informada.
				
**Função 3**
- Comparar cada item da lista de nomes de arquivos, desconsiderando a sua extensão junto com o ponto separador ('.'), com cada item da lista de nomes das colunas:
	- Caso os valores sejam iguais:
		- Acessar diretório do arquivo
		- Copiar o arquivo para diretório informado como destino de cópia.

### 6.3. Banco de Dados
**Na camada de persistencia, é necessário realizar insert de dados nos SGBD's SQL Server e no Postgresql de forma independente.**
- Definições
- -Definições
