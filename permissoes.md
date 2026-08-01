# 🔐 Permissões e Proprietários

Nesta etapa foram praticados comandos fundamentais para gerenciamento de permissões, proprietários e grupos associados a arquivos no Linux.

O sistema de permissões do Linux permite definir diferentes níveis de acesso para o **usuário proprietário**, o **grupo** e os **outros usuários** do sistema.

---

## 📋 `ls -l` — Visualizar permissões

O comando `ls -l` apresenta informações detalhadas sobre arquivos e diretórios, incluindo suas permissões, proprietário e grupo.

```bash
ls -l
```

As permissões são representadas por uma sequência de caracteres. Por exemplo:

```text
-rw-r--r--
```

A estrutura pode ser dividida em três conjuntos principais:

| Permissão | Significado        |
| --------- | ------------------ |
| `r`       | Read — leitura     |
| `w`       | Write — escrita    |
| `x`       | Execute — execução |

Os três conjuntos correspondem a:

```text
Usuário (owner) | Grupo (group) | Outros (others)
```

Por exemplo:

```text
-rw-r--r--
 │││ │││ └── Outros: leitura
 │││ └┴┴──── Grupo: leitura
 │┴┴──────── Usuário: leitura e escrita
```

---

## 📄 Criando um arquivo para testar permissões

Foi criado o arquivo `permissoes.txt` utilizando o comando `touch`.

```bash
touch permissoes.txt
```

Em seguida, o comando `ls -l` foi utilizado para verificar as permissões iniciais do arquivo.

---

## 🔢 `chmod` — Alterar permissões

O comando `chmod` (*Change Mode*) permite alterar as permissões de arquivos e diretórios.

Neste laboratório, foram utilizados dois conjuntos de permissões através da notação octal.

### Permissão `600`

```bash
chmod 600 permissoes.txt
```

A permissão `600` significa:

```text
Usuário: leitura + escrita
Grupo:   sem permissões
Outros:  sem permissões
```

Representação:

```text
-rw-------
```

### Permissão `644`

Depois, a permissão foi alterada para `644`:

```bash
chmod 644 permissoes.txt
```

A permissão `644` significa:

```text
Usuário: leitura + escrita
Grupo:   leitura
Outros:  leitura
```

Representação:

```text
-rw-r--r--
```

Essa é uma configuração bastante comum para arquivos que precisam ser lidos por outros usuários, mas modificados apenas pelo proprietário.

---

## 👥 `chgrp` — Alterar o grupo

O comando `chgrp` (*Change Group*) permite alterar o grupo associado a um arquivo ou diretório.

No laboratório, o grupo do arquivo foi alterado para `suporte-ti`:

```bash
sudo chgrp suporte-ti permissoes.txt
```

Depois, `ls -l` foi utilizado para verificar a alteração.

---

## 👤 `chown` — Alterar o proprietário

O comando `chown` (*Change Owner*) permite alterar o proprietário de um arquivo ou diretório.

Primeiramente, o proprietário do arquivo foi alterado para o usuário `suporte`:

```bash
sudo chown suporte permissoes.txt
```

Depois, o proprietário e o grupo foram definidos juntos:

```bash
sudo chown suporte:suporte-ti permissoes.txt
```

A utilização de `chown` dessa forma permite definir simultaneamente o usuário proprietário e o grupo associado ao arquivo.

---

## 📸 Evidência da prática

A imagem abaixo apresenta o registro completo da atividade prática, incluindo a criação do arquivo `permissoes.txt`, alteração das permissões com `chmod`, mudança do grupo com `chgrp` e alteração do proprietário com `chown`.

![Prática completa de permissões e proprietários](https://github.com/user-attachments/assets/08339411-0bc3-4abc-be95-873525404cbf)
---

## 📌 Resumo dos comandos

| Comando | Função                                                      |
| ------- | ----------------------------------------------------------- |
| `ls -l` | Exibe permissões, proprietário, grupo e outras informações  |
| `chmod` | Altera as permissões de arquivos e diretórios               |
| `chgrp` | Altera o grupo associado a um arquivo ou diretório          |
| `chown` | Altera o proprietário e/ou grupo de um arquivo ou diretório |

---

## 💡 Conceitos praticados

* Permissões de leitura (`r`);
* Permissões de escrita (`w`);
* Permissões de execução (`x`);
* Usuário proprietário (*owner*);
* Grupo (*group*);
* Outros usuários (*others*);
* Notação octal de permissões;
* Alteração de permissões com `chmod`;
* Alteração de grupos com `chgrp`;
* Alteração de proprietário com `chown`.
