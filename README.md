# 🐧 Linux Lab — Administração e Troubleshooting

![Linux Ubuntu](https://img.shields.io/badge/Linux-Ubuntu_24.04-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
![VirtualBox](https://img.shields.io/badge/VirtualBox-VM-183A61?style=for-the-badge&logo=virtualbox&logoColor=white)
![Bash Shell](https://img.shields.io/badge/Shell_Script-Bash-4EAA25?style=for-the-badge&logo=gnu-bash&logoColor=white)
![Git](https://img.shields.io/badge/Git-Repository-F05032?style=for-the-badge&logo=git&logoColor=white)

Laboratório prático desenvolvido para estudar, praticar e documentar os fundamentos de administração de sistemas, gerenciamento de permissões e diagnóstico de problemas (*troubleshooting*) em ambientes Linux.

---

## 🎯 Objetivo

Consolidar conhecimentos práticos de Linux essenciais para a rotina de suporte técnico e infraestrutura. O foco do projeto foi executar comandos diretamente no terminal Bash, simulando tarefas diárias de administração do sistema, como gestão de usuários, monitoramento de processos, análise de recursos e testes de conectividade.

---

## 🖥️ Ambiente Utilizado

* **Sistema Operacional:** Ubuntu Linux 24.04 LTS
* **Virtualização:** Oracle VM VirtualBox
* **Interface:** Terminal Bash (`/bin/bash`)
* **Usuário do Lab:** `oliveira` / `suporte`

---

## 📚 Conteúdos e Comandos Praticados

### 📂 1. Navegação e Manipulação de Arquivos
Navegação na árvore de diretórios, criação, cópia, movimentação e remoção de arquivos e pastas.
```bash
pwd ls ls -la cd mkdir touch cp mv rm
```

### 👤 2. Usuários e Grupos
Criação e gerenciamento de contas de usuários, criação de grupos e associação de usuários a grupos secundários.
```bash
whoami id adduser groupadd usermod groups
```

### 🔐 3. Permissões e Proprietários
Visualização e alteração de permissões de leitura, escrita e execução em arquivos e diretórios, além de alteração de proprietário e grupo.
```bash
ls -l chmod chown chgrp
```

### ⚙️ 4. Processos e Recursos
Listagem e monitoramento de processos, execução de tarefas em segundo plano (*background*) e encerramento de processos travados ou desnecessários.
```bash
ps aux top htop kill sleep 300 &
```

### 💾 5. Memória e Armazenamento
Análise de uso da memória RAM e Swap, diagnóstico de ocupação de disco, verificação de espaço em diretórios e listagem de blocos e partições montadas.
```bash
free -h df -h du -sh lsblk mount
```

### 🌐 6. Diagnóstico de Redes e Conectividade
Mapeamento de interfaces e endereços IP, verificação de rotas padrão, testes de conectividade com pacotes ICMP, análise de conexões/portas ativas e requisições HTTP via terminal.
```bash
ip a ip r ping ss -tulnp curl
```

---

## 🗂️ Estrutura do Repositório

```text
linux-lab/
├── README.md
├── navegacao.md
