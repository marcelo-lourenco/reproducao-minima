# Reprodução Mínima

## O que é um repositório de reprodução mínima?

Um repositório de reprodução mínima é um repositório Git que pode ser compartilhado publicamente (não expõe lógica de negócios privada), demonstra o problema que você está enfrentando e possui o mínimo de dependências instaladas possível. Ele também contém os passos para replicar o erro que você está encontrando. É mais fácil adicionar isso ao arquivo README, mas você pode adicioná-lo em qualquer lugar, até mesmo em um arquivo de texto.

## Não expõe lógica de negócios

Parece bem simples, certo? Se seu erro está relacionado a uma etapa específica na lógica de negócios, replique a lógica de negócios de forma que não revele o que você está trabalhando.

## Demonstra o problema que você está enfrentando

Precisa de explicação? É por isso que a reprodução mínima deve ser criada em primeiro lugar, porque você tem um erro que quer que alguém investigue.

## Possui o mínimo de dependências instaladas possível

Se a reprodução não precisa de algo, remova-o. Bancos de dados são frequentemente fáceis de remover em uma reprodução mínima. Sério, quanto menos você fizer os outros configurarem bancos de dados, mais fácil será trabalhar com isso. Se você acabar tendo um problema relacionado ao banco de dados ou um problema entre vários servidores, adicionar um arquivo `docker-compose.yml` para orquestrar as conexões ajuda muito.

## Passos para replicar

Um conjunto de passos claros e definidos sobre como replicar o erro. Você também pode separar os passos de configuração e reprodução, se quiser. Um exemplo seria algo como:

```
# Configuração

1) npm install

# Reprodução

1) npm run start:dev
2) abrir um novo terminal
3) curl http://localhost:3000/users
4) verificar o erro
```

## Ok, entendi o que é, o que mais preciso?

Em geral, se você atender o exemplo acima, está pronto. Isso ajuda muito aqueles que depuram erros e fornecem suporte.

## Por que estou sendo solicitado a fornecer isso?

Existem alguns motivos para fornecer uma reprodução mínima:

1. torna muito mais fácil depurar onde o erro _poderia_ estar. Em vez de procurar em 20 arquivos e 5 diretórios, agora são apenas 2 arquivos em 1 diretório. Muito menos para analisar e entender.
2. metade das vezes, ao criar a reprodução mínima, você mesmo encontrará o problema e crescerá como desenvolvedor e como compartilhador de conhecimento.

* [Confira a definição de reprodução mínima do StackOverflow](https://stackoverflow.com/help/minimal-reproducible-example)
