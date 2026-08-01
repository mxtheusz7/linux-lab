# 📂 Navegação e Manipulação de Arquivos

Nesta etapa foram praticados comandos fundamentais para navegar pelo sistema de arquivos Linux e realizar operações básicas com diretórios e arquivos.

---

## 📍 Navegação no sistema

O comando `pwd` (*Print Working Directory*) exibe o caminho completo do diretório atual.

```bash id="b9eg4j"
pwd
```

O comando `ls` lista os arquivos e diretórios presentes no local atual. Já o `ls -la` apresenta uma listagem detalhada, incluindo arquivos e diretórios ocultos.

```bash id="3p2ux7"
ls
ls -la
```

O comando `cd` (*Change Directory*) permite navegar entre diretórios.

```bash id="9r0j2p"
cd linux-lab
```

---

## 📁 Criação de diretórios e arquivos

O comando `mkdir` (*Make Directory*) é utilizado para criar diretórios. No laboratório, foi criado o diretório `linux-lab` para organizar as atividades práticas.

```bash id="1xjndq"
mkdir linux-lab
```

O comando `touch` foi utilizado para criar o arquivo vazio `exemplo.txt`.

```bash id="b3j6si"
touch exemplo.txt
```

O comando `ls` foi utilizado novamente para verificar os arquivos existentes, enquanto `ls -l` permitiu visualizar informações detalhadas sobre o arquivo.

```bash id="1w7k2r"
ls
ls -l
```

---

## 📦 Copiando e movendo arquivos

O comando `cp` (*Copy*) foi utilizado para criar uma cópia do arquivo `exemplo.txt`.

```bash id="l8x0cr"
cp exemplo.txt copia.txt
```

Em seguida, o comando `mkdir` foi utilizado para criar o diretório `backup`.

```bash id="h3h5qf"
mkdir backup
```

O comando `mv` (*Move*) foi utilizado para mover o arquivo `copia.txt` para dentro do diretório `backup`.

```bash id="v3q8nk"
mv copia.txt backup/
```

Os comandos `ls` e `ls backup` foram utilizados para verificar o resultado das operações.

```bash id="b6b7d2"
ls
ls backup
```

---

## 🗑️ Removendo arquivos

Por fim, o comando `rm` (*Remove*) foi utilizado para remover o arquivo `exemplo.txt`.

```bash id="q9w8ec"
rm exemplo.txt
```

Após a remoção, o comando `ls` foi utilizado para confirmar o estado final do diretório.

```bash id="z2c5pa"
ls
```

---

## 📸 Evidência da prática

A imagem abaixo apresenta o registro completo da atividade prática, desde a navegação inicial no sistema até a criação, cópia, movimentação e remoção de arquivos.

![Prática completa de navegação e manipulação de arquivos](images/navegacao/01-navegacao-completa.png)

---

## 📌 Resumo dos comandos

| Comando  | Função                                                                     |
| -------- | -------------------------------------------------------------------------- |
| `pwd`    | Exibe o diretório atual                                                    |
| `ls`     | Lista arquivos e diretórios                                                |
| `ls -la` | Lista arquivos e diretórios, incluindo ocultos, com informações detalhadas |
| `cd`     | Navega entre diretórios                                                    |
| `mkdir`  | Cria diretórios                                                            |
| `touch`  | Cria arquivos vazios                                                       |
| `cp`     | Copia arquivos e diretórios                                                |
| `mv`     | Move ou renomeia arquivos e diretórios                                     |
| `rm`     | Remove arquivos                                                            |
