# Migração de SQLite3 para Mysql

## Como gerar um Dump (export) do SQLite na linha de comando

```bash
sqlite3 [database.sqlite3] .dump > [destino.sql]
```

Examplo:

```bash
sqlite3 db.sqlite3 .dump > dump-sqlite.sql
```

Para adicionar permissão de execução ao arquivo:

```bash
chmod +x [nome-arquivo]
```

## Como traduzir de SQLite dialeto para MySQL dialeto

Executa o script em Python ou em Perl:

```bash
python migra.py [dump-origem] > [dump-destino]
```

Exemplo:

```bash
python migra.py dump-sqlite.sql > dump-mysql.sql
```