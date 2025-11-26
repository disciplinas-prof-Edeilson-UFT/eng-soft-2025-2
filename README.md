# Engenharia de Software 2025/2

## Universidade Federal do Tocantins - Palmas

---

**Curso:** Bacharelado em Ciência da Computação

**Professor:** Dr. Edeilson Milhomem da Silva

---

## Grupos:

### Grupo: DinDIn 💸

**Membros/Integrantes:**

* Cristian
* Gabriel Portuguez
* Thales
* Vinicius Fernandes
---

## Projeto: DinDIn - Gerenciamento Financeiro

O **DinDin** é um aplicativo web simples e intuitivo para **gerenciamento de finanças pessoais e empresariais**.

O foco é ajudar o usuário a **controlar receitas e despesas**, organizar em **categorias personalizadas** e manter uma **visão clara do saldo mensal**. Nosso MVP (Produto Mínimo Viável) oferece controle financeiro prático e acessível, entregando valor desde o primeiro uso.

**Com o DinDin, você pode:**

* Criar sua conta e acessar de forma segura 🔐
* Registrar receitas e despesas de maneira rápida 💵
* Organizar seus lançamentos por categorias 📂
* Consultar histórico de transações e filtros 🔎
* Acompanhar saldo do mês em tempo real 📊

---

## 🔗 Acesso ao Repositório

O código-fonte e o histórico de desenvolvimento deste projeto podem ser encontrados no seguinte endereço:

**Link do GitHub:** [Clique](https://github.com/Thales-uft2022-2/DinDin/)

---
LandingPage: [Clique](https://thales-uft2022-2.github.io/DinDin/)
---
[Apresentação Final da Disciplina](#)
---
# 🛠️ Guia de Configuração e Instalação (Developer Setup)

Este documento contém as instruções passo a passo para configurar o ambiente de desenvolvimento do projeto DinDin em sua máquina local.

## 📋 Pré-requisitos

Antes de começar, certifique-se de ter as seguintes ferramentas instaladas:

- **XAMPP** (ou similar com Apache e MySQL) - [Download](https://www.apachefriends.org/)
  - *Recomendado: PHP 8.1 ou superior*
- **Composer** (Gerenciador de dependências do PHP) 
- **Git**  
- **Editor de Código** (VS Code recomendado)

## 🚀 Passo a Passo da Instalação

### 1. Clonar o Repositório

Abra seu terminal (Git Bash ou CMD) e clone o projeto para a sua máquina.

Se você estiver usando XAMPP, o ideal é clonar diretamente dentro da pasta `htdocs`:

```
bash cd C:\xampp\htdocs git clone https://github.com/Thales-uft2022-2/DinDin
cd DinDin.
```


### 2. Instalar Dependências (Backend)

O projeto utiliza o Composer para gerenciar bibliotecas (como o PHPMailer e o PHPUnit). Na raiz do projeto (dentro da pasta DinDin), execute:
```
composer install phpunit
composer install phpmailer
```
Isso criará a pasta `vendor/` com todas as bibliotecas necessárias.

### 3. Configurar o Banco de Dados

1. Inicie o Apache e o MySQL no painel de controle do XAMPP
2. Acesse o phpMyAdmin no navegador: `http://localhost/phpmyadmin`
3. Crie um novo banco de dados chamado `dindin` (ou o nome definido no seu config.php)
   - *Collation recomendada: `utf8mb4_unicode_ci`*
4. Importe o esquema do banco:
   - Selecione o banco criado
   - Vá na aba **Importar**
   - Escolha o arquivo `dindin.sql` localizado na raiz do projeto
   - Clique em **Executar**

### 4. Configurar Variáveis de Ambiente

Verifique o arquivo `config/config.php` (ou crie um arquivo `.env` se o projeto utilizar) para garantir que as credenciais do banco estão corretas para o seu ambiente XAMPP padrão.

**Exemplo padrão do XAMPP:**
- **Host:** `localhost`
- **User:** `root`
- **Password:** `` (vazio)
- **Database:** `dindin`

### 5. Executar o Projeto

Com o Apache do XAMPP rodando e os arquivos na pasta `htdocs`, acesse o projeto pelo navegador:


```http://localhost/DinDin/public```

> **Nota:** O ponto de entrada da aplicação é a pasta `/public`. Se você acessar apenas `/DinDin`, navegue até a pasta `public`.

## 🧪 Rodando os Testes (PHPUnit)

Para garantir que tudo está funcionando corretamente, execute os testes unitários.

No terminal, na raiz do projeto:

bash
```./vendor/bin/phpunit```

Se todos os testes passarem (✅ **ficar verde**), seu ambiente está configurado e pronto para o desenvolvimento!

## 📂 Estrutura de Pastas Importantes

- `app/` - Lógica do sistema (Controllers, Models, Services)
- `public/` - Arquivos acessíveis publicamente (CSS, JS, Index.php)
- `config/` - Arquivos de configuração (Banco de dados, etc)
- `views/` - Telas e templates HTML/PHP
- `tests/` - Testes unitários---

