#### Arquitetura do Sistema Back-End

## Visão da Estrutura de Diretórios

A estrutura de diretórios para o projeto deve ser organizada da seguinte forma:

```plaintext
project_root/                  >> Diretório raiz do projeto.
│
├── src/                       >> Contém todo o código-fonte do projeto.
│   ├── main.py                >> Arquivo principal que executa o fluxo da aplicação.
│   ├── data_processing/             >> Pacote com os módulos de processamento de dados.
│   │   ├── __init__.py                     >> 
│   │   ├── file_reader.py                  >> Módulo responsável pela leitura dos arquivos.
│   │   ├── file_comparator.py              >> Módulo responsável pela comparação dos arquivos.
│   │   └── file_copier.py                  >> Módulo responsável pela cópia dos arquivos.
│   ├── utils/                       >> Pacote com módulos utilitários.                   
│   │   ├── __init__.py                     >> 
│   │   ├── logger.py                       >> Módulo para configuração de logs.
│   │   ├── logger.py                       >> Módulo para configuração do projeto.
│   └── tests/                       >> Pacote para os testes unitários.
│       ├── __init__.py                     >>
│       ├── test_file_reader.py             >> Pacote para os testes unitários.
│       ├── test_file_comparator.py         >> Testes para o módulo de comparação de arquivos.
│       └── test_file_copier.py             >> Testes para o módulo de cópia de arquivos.
│
├── data/                            >> Diretório para armazenar os dados utilizados e gerados pelo projeto.
│   ├── input/                          >> Contém os arquivos de entrada.
│   ├── output/                         >> Contém os arquivos de saída.
│   └── reference/                      >> Contém os arquivos de referência.
│
├── requirements.txt                        >> Lista de dependências do projeto.
├── README.md                               >> Arquivo de documentação do projeto.
└── .gitignore                              >> Arquivo para especificar quais arquivos/directórios devem ser ignorados pelo Git.
```
## Criando Estrutura de Diretórios no VS Code
- **Diretório Principal:** D:\VisualStudioCode\pa-siasus
- Via Terminal PorwerShell

**Antes de criar a estrutura de diretórios e os arquivos do projeto, é uma prática recomendada criar um ambiente virtual para isolar as dependências do projeto.**

### 1. Criar o ambiente virtual :
- #### Navegar até o diretório onde deseja criar o ambiente virtual
  *PS D:\VisualStudioCode\pa-siasus>* ```cd D:\VisualStudioCode\pa-siasus```
- #### Criar o ambiente virtual
  *PS D:\VisualStudioCode\pa-siasus>* ```python -m venv venv```

### 2. Ativar o ambiente virtual:
- #### Ativar o ambiente virtual no Windows
  *PS D:\VisualStudioCode\pa-siasus>* ```.\venv\Scripts\Activate.ps1```

### 3. Criar a estrutura de diretórios e arquivos do projeto:
- #### Criar diretórios
```
  mkdir src
  mkdir src/data_processing
  mkdir src/utils
  mkdir src/tests
  mkdir data
  mkdir data/input
  mkdir data/output
  mkdir data/reference
```
- #### Criar arquivos dentro de src
```
  New-Item -ItemType file .\src\__init__.py
  New-Item -ItemType file .\src\main.py
  New-Item -ItemType file .\src\config.py
  New-Item -ItemType file .\src\file_handler.py
  New-Item -ItemType file .\src\column_comparator.py
  New-Item -ItemType file .\src\utils.py
```
- #### Criar arquivos dentro de tests
```
  New-Item -ItemType file .\src\tests\__init__.py
  New-Item -ItemType file .\src\tests\test_file_handler.py
  New-Item -ItemType file .\src\tests\test_column_comparator.py
  New-Item -ItemType file .\src\tests\test_utils.py
```
- #### Criar arquivos adicionais
```
New-Item -ItemType file .\requirements.txt
New-Item -ItemType file .\README.md
```

