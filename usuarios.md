# 👤 Usuários e Grupos

Nesta etapa foram praticados comandos básicos para identificação e gerenciamento de usuários e grupos em um sistema Linux.

O gerenciamento de usuários e grupos é importante para organizar o acesso ao sistema e controlar a associação de contas a diferentes grupos.

---

## 🔎 `whoami` — Identificar o usuário atual

O comando `whoami` exibe o nome do usuário atualmente conectado à sessão do terminal.

```bash
whoami
```

No laboratório, o comando foi utilizado para confirmar que a sessão estava sendo executada pelo usuário `oliveira`.

---

## 🆔 `id` — Identificar usuário e grupos

O comando `id` exibe informações sobre a identidade do usuário, incluindo:

* `UID` — identificador do usuário;
* `GID` — identificador do grupo principal;
* Grupos adicionais aos quais o usuário pertence.

```bash
id
```

No laboratório, o comando foi utilizado para visualizar as informações do usuário `oliveira` e seus grupos associados.

---

## 👤 `adduser` — Criar um usuário

O comando `adduser` é utilizado para criar uma nova conta de usuário no sistema.

```bash
sudo adduser suporte
```

Durante a criação do usuário `suporte`, foi definida uma senha e foram solicitadas informações adicionais sobre a conta.

O usuário foi criado com o objetivo de ser utilizado nas atividades práticas de gerenciamento de usuários e grupos.

---

## 👥 `groupadd` — Criar um grupo

O comando `groupadd` permite criar um novo grupo no sistema.

```bash
sudo groupadd suporte-ti
```

No laboratório, foi criado o grupo `suporte-ti`, utilizado para demonstrar a associação de um usuário a um grupo secundário.

---

## 🔗 `usermod -aG` — Adicionar usuário a um grupo

O comando `usermod` permite modificar as configurações de uma conta de usuário.

A opção `-aG` é utilizada para adicionar o usuário a um grupo secundário, mantendo os grupos aos quais ele já pertence.

```bash
sudo usermod -aG suporte-ti suporte
```

Nesse exemplo, o usuário `suporte` foi adicionado ao grupo secundário `suporte-ti`.

---

## 📋 `groups` — Verificar grupos do usuário

O comando `groups` mostra os grupos aos quais um usuário pertence.

```bash
groups suporte
```

O resultado confirmou que o usuário `suporte` pertence ao seu grupo principal e também ao grupo secundário `suporte-ti`.

---

## 📸 Evidência da prática

A imagem abaixo apresenta o registro completo da atividade prática realizada no terminal, incluindo a identificação do usuário atual, consulta de informações de identidade, criação do usuário `suporte`, criação do grupo `suporte-ti` e associação do usuário ao grupo.

![Prática completa de usuários e grupos](https://github.com/user-attachments/assets/12cf23c3-a085-4517-82a1-3c31d01a355f)
---

## 📌 Resumo dos comandos

| Comando       | Função                                        |
| ------------- | --------------------------------------------- |
| `whoami`      | Exibe o nome do usuário atual                 |
| `id`          | Exibe UID, GID e grupos associados ao usuário |
| `adduser`     | Cria uma nova conta de usuário                |
| `groupadd`    | Cria um novo grupo                            |
| `usermod -aG` | Adiciona um usuário a um grupo secundário     |
| `groups`      | Exibe os grupos aos quais um usuário pertence |

---

## 💡 Conceitos praticados

* Identificação de usuários no Linux;
* UID e GID;
* Criação de contas de usuário;
* Criação de grupos;
* Grupos principais e secundários;
* Associação de usuários a grupos;
* Verificação de grupos associados a uma conta.
