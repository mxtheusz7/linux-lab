# 🐧 Linux Lab — Administração e Troubleshooting

![Linux Ubuntu](https://img.shields.io/badge/Linux-Ubuntu_24.04-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
![VirtualBox](https://img.shields.io/badge/VirtualBox-VM-183A61?style=for-the-badge&logo=virtualbox&logoColor=white)
![Bash Shell](https://img.shields.io/badge/Shell_Script-Bash-4EAA25?style=for-the-badge&logo=gnu-bash&logoColor=white)
![Git](https://img.shields.io/badge/Git-Repository-F05032?style=for-the-badge&logo=git&logoColor=white)

Laboratório prático desenvolvido para estudar, praticar e documentar os fundamentos de administração de sistemas, gerenciamento de privilégios e diagnóstico de problemas (*troubleshooting*) em ambientes Linux.

---

## 🎯 Objetivo

Consolidar conhecimentos práticos de Linux essenciais para a rotina de suporte técnico, infraestrutura e segurança da informação. O foco do projeto foi executar comandos diretamente no terminal Bash, simulando tarefas diárias de sysadmin como controle de acesso, auditoria de processos, análise de recursos e diagnósticos de conectividade.

---

## 🖥️ Ambiente Utilizado

* **Sistema Operacional:** Ubuntu Linux 24.04 LTS
* **Virtualização:** Oracle VM VirtualBox
* **Interface:** Terminal Bash (`/bin/bash`)
* **Usuário do Lab:** `oliveira` / `suporte`

---

## 📚 Conteúdos e Comandos Praticados

### 📂 1. Navegação e Manipulação de Arquivos
Navegação na árvore de diretórios, criação, cópia, movimentação e remoção segura de arquivos e pastas.
```bash
pwd ls ls -la cd mkdir touch cp mv rm
```

### 👤 2. Usuários, Grupos e Privilégios
Criação e gestão de contas de usuários, administração de grupos secundários e verificação de privilégios e identidades (`UID`/`GID`).
```bash
whoami id adduser groupadd usermod groups su
```

### 🔐 3. Permissões e Proprietários
Configuração de permissões de leitura, escrita e execução em notação octal e alteração de proprietário e grupo de arquivos.
```bash
ls -l chmod chown chgrp
```

### ⚙️ 4. Processos e Gerenciamento de Tarefas
Execução de processos em segundo plano (*background*), monitoramento de PIDs e encerramento de tarefas via sinais do Kernel.
```bash
ps aux top htop kill sleep &
```

### 💾 5. Armazenamento e Memória
Análise do consumo de memória RAM, utilização do espaço de Swap e diagnóstico de ocupação de disco e partições montadas.
```bash
free -h df -h du -sh
```

### 🌐 6. Diagnóstico de Redes e Conectividade
Mapeamento de interfaces de rede, validação da rota padrão (gateway), testes de conectividade ICMP, verificação de portas escutando (`LISTEN`) e testes HTTP via terminal.
```bash
ip a ip r ping ss -tulnp curl
```

---

## 🗂️ Estrutura do Repositório

```text
linux-lab/
├── README.md
├── navegacao.md
├── usuarios.md
├── permissoes.md
├── processos.md
├── armazenamento.md
├── rede.md
└── images/
    ├── navegacao/
    ├── usuarios/
    ├── permissoes/
    ├── processos/
    ├── armazenamento/
    └── rede/
```

---

## 🛠️ Competências Desenvolvidas

* **Administração Básica:** Operação de sistemas operacionais baseados em Linux via CLI.
* **Gestão de Identidade (IAM):** Provisionamento de usuários e controle de acesso granular com grupos.
* **Segurança de Arquivos:** Aplicação do princípio do menor privilégio (*Least Privilege*) usando `chmod` e `chown`.
* **Troubleshooting de Desempenho:** Identificação de gargalos em CPU, memória RAM e disco.
* **Análise de Conectividade:** Validação do stack TCP/IP, serviços de rede ativos e respostas de requisições web.

---

📌 *Este projeto possui caráter estritamente educacional e faz parte do meu portfólio prático de estudos em Tecnologia da Informação e Segurança.*
