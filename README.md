# BANCO_DE_DADOS_PICOLE_ASSINCRONO 

**Modelagem e criação de banco de dados SQLite ou MySQL de forma assíncrona com SQL Alchemy**

- SQLAlchemy é uma biblioteca de ORM (Object-Relational Mapping) em Python que permite interagir com bancos de dados usando classes e objetos, abstraindo as consultas SQL complexas. Além de oferece ferramentas para executar consultas em SQL diretamente.

- Em BANCO_DE_DADOS_PICOLES_ASSINCRONO é possível alternar uma modelagem de banco de dados relacional complexa para diferentes bancos como SQLite, MySQL, PostgreSQL, Microsoft SQL Server, Oracle Database e etc, com apenas uma ou duas linhas de código, sem necessidade de reestruturar ou ajustar as diferentes peculiaridades dos diferentes SGBD (Sistema de Gerenciamento de Banco de Dados), em resumo não ha necessidade de alterações em consultas dos diferentes Banco de Dados. 

- Neste projeto alterne o banco de dados de nome "picoles_async" para SQLite ou MySQL como uma unica linha de código, seguindo os passos abaixo:

    - Acesse o código: "D:\conf\config_DB.py"

    - Vá até a função: "async def criar_tabelas() -> None:"

    - Alterne os bancos de dados apenas comentando as linhas abaixo:

        if not __async_engine:
            await criar_banco_de_dados() # MySQL (Banco ativo)
            # await criar_banco_de_dados(sqlite=True) # SQLite (linha comentada)

![Relacionamento do banco de dados.pmg](<Relacionamento do banco de dados.png>)

- Principais tecnologias:
    - SQLAlchemy é uma biblioteca ORM (Object-Relational Mapping).
    - Módulo asyncio que é usado para escrever código assíncrono,  onde devido grande volume de dados pode ocorrer atraso de resposta.