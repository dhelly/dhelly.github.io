---
layout: post
title:  "Notificação por email Usando o Composer"
date:   2020-10-30 17:00:00 -0300
categories: php composer git packagist
---

Criando um projeto com composer

## Descrição
Este repositório tem como finalidade aplicar o conhecimento do [Curso Composer na Prática](https://www.upinside.com.br/cursos/composer-na-pratica) da [UpInside Treinamentos](https://www.upinside.com.br).

## Anotações

Iniciando um projeto
> composer init

Prencher os dados solicitados
- This is a library that uses composer as the basis for generating email notification
- dev

Resultado final:
```json
{
    "name": "jaqueline/notification",
    "description": "This is a library that uses composer as the basis for generating email notification",
    "type": "library",
    "license": "MIT",
    "authors": [
        {
            "name": "Jaqueline Fernandes",
            "email": "dhelly@gmail.com",
            "homepage": "https://jaqueline.dev",
            "role": "Developer"
        }
    ],
    "minimum-stability": "dev",
    "require": {}
}
```

Instalando um biblioteca
> composer require phpmailer/phpmailer

Remover uma biblioteca
> composer remove phpmailer/phpmailer

Alterando no nome da pasta *vendor*
```json
{
    "name": "jaqueline/notification",
    "description": "This is a library that uses composer as the basis for generating email notification",
    "type": "library",
    "license": "MIT",
    "authors": [{
        "name": "Jaqueline Fernandes",
        "email": "dhelly@gmail.com",
        "homepage": "https://jaqueline.dev",
        "role": "Developer"
    }],
    "minimum-stability": "dev",
    "require": {
        "phpmailer/phpmailer": "6.1.8"
    },
    "config": {
        "vendor-dir": "lib_ext"
    }
}
```
Executamos o comando `composer update`

## Enviado nosso projeto para o git

1 - Criamos nosso repositório no github
2 - Adicionamos nosso projeto ao git `git init`
3 - Adicionamos o nosso repositório remoto ao nosso projeto
> git remote add origin <endereço do repositório>

4 - Puxar o arquivo `readme.md` criado pelo git para não precisar fazer merger da nossa branch

> git pull origin main --allow-unrelated-histories

4 - Criar um arquivo `.gitignore`. Se quiser gerar automaticamente um use o link abaixo.
> https://www.toptal.com/developers/gitignore

Devemos lembrar de alterar a pasta `vendor` para `lib_ext` para não entrar no controle de versionamento.

5 - Adicionar todos os arquivos.
> git add .

6 - Commitar o projeto no git
> git commit -m "mensagem"

7 - Enviar para o github
> git push origin main

## Readme.md
Melhorar o `readme.md`, pois ele será utilizado pelo **packagist**.

Vamos utilizar o modelo fornecido pelo instrutor. Podemos formatar na própria IDE(no meu caso VSCODE) o usando o site [dillinger](https://dillinger.io/)

## Publicação no [Packagist](https://packagist.org)

Primeiro criamos um conta. Com o repositório do github escolhemos a opção `submit`.

[Repositório no Github](https://github.com/dhelly/notification)
