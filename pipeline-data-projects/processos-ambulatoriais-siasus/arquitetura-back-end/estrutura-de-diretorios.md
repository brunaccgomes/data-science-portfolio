#### Arquitetura do Sistema Back-End

## Estrutura de Diretórios

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
