#### Arquitetura do Sistema Back-End

## Estrutura de Diretórios

A estrutura de diretórios para o projeto deve ser organizada da seguinte forma:

```plaintext
project_root/
│
├── src/
│   ├── main.py
│   ├── data_processing/
│   │   ├── __init__.py
│   │   ├── file_reader.py
│   │   ├── file_comparator.py
│   │   └── file_copier.py
│   ├── utils/
│   │   ├── __init__.py
│   │   ├── logger.py
│   │   └── config.py
│   └── tests/
│       ├── __init__.py
│       ├── test_file_reader.py
│       ├── test_file_comparator.py
│       └── test_file_copier.py
│
├── data/
│   ├── input/
│   ├── output/
│   └── reference/
│
├── requirements.txt
├── README.md
└── .gitignore
