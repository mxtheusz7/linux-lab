# 🌐 Diagnóstico de Redes e Conectividade

Nesta etapa foram praticados comandos básicos para análise de interfaces de rede, endereçamento IP, rotas, conectividade, conexões de rede e requisições HTTP no Linux.

Esses comandos são importantes para atividades de suporte técnico, infraestrutura e troubleshooting, permitindo identificar configurações de rede e verificar possíveis problemas de conectividade.

---

## 🌐 `ip a` — Verificar interfaces e endereços IP

O comando `ip a` exibe informações sobre as interfaces de rede disponíveis no sistema e seus respectivos endereços IP.

```bash
ip a
```

A saída permite identificar informações como:

* Interfaces de rede;
* Endereços IPv4 e IPv6;
* Estado das interfaces;
* Endereço MAC;
* Interface de loopback (`lo`).

Esse comando é útil para verificar se uma interface de rede está ativa e identificar o endereço IP atribuído ao sistema.

---

## 🛣️ `ip r` — Verificar rotas de rede

O comando `ip r` exibe a tabela de roteamento do sistema.

```bash
ip r
```

Através desse comando é possível identificar informações como:

* Rota padrão (*default route*);
* Gateway utilizado;
* Interfaces associadas às rotas;
* Redes diretamente conectadas.

A rota padrão é importante para determinar por onde o sistema encaminha pacotes destinados a redes externas.

---

## 📡 `ping` — Testar conectividade

O comando `ping` é utilizado para testar a conectividade entre o computador e outro dispositivo ou servidor através de pacotes ICMP.

```bash
ping google.com
```

Durante a prática, o domínio `google.com` foi utilizado para verificar se o sistema conseguia alcançar um servidor externo.

O resultado permite observar:

* Respostas recebidas;
* Tempo de resposta;
* Perda de pacotes;
* Conectividade com o destino.

Esse comando é uma das ferramentas mais utilizadas para diagnóstico inicial de problemas de rede.

---

## 📸 Evidência prática — `ip a`, `ip r` e `ping`

O print abaixo apresenta a execução dos comandos `ip a`, `ip r` e `ping google.com` durante a atividade prática, permitindo observar as interfaces de rede, a tabela de roteamento e o teste de conectividade.

![Análise de interfaces, rotas e conectividade](https://github.com/user-attachments/assets/6aaffa07-51d8-47ab-941a-726e432a03ed)

---

## 🔌 `ss -tulnp` — Verificar conexões e portas

O comando `ss` permite visualizar informações sobre sockets e conexões de rede.

```bash
ss -tulnp
```

As opções utilizadas permitem analisar:

* `-t` — conexões TCP;
* `-u` — conexões UDP;
* `-l` — portas em estado de escuta (*LISTEN*);
* `-n` — exibe endereços e portas numericamente;
* `-p` — exibe informações dos processos associados.

Esse comando é útil para identificar serviços que estão escutando em determinadas portas e auxiliar no diagnóstico de problemas relacionados a serviços de rede.

### 📸 Evidência prática

![Verificação de conexões e portas com ss -tulnp](https://github.com/user-attachments/assets/7e2b2060-f7e0-43f1-8102-4311f66ac24f)

---

## 🌍 `curl` — Realizar requisições HTTP

O comando `curl` permite realizar requisições e transferências de dados utilizando diferentes protocolos, sendo bastante utilizado para testar serviços web e APIs.

```bash
curl google.com
```

Durante a prática, o comando foi utilizado para realizar uma requisição ao domínio `google.com`.

Essa prática permite verificar se o sistema consegue estabelecer comunicação com um servidor web e receber uma resposta.

O `curl` também é uma ferramenta bastante utilizada em troubleshooting para testar serviços HTTP e APIs diretamente pelo terminal.

### 📸 Evidência prática

![Requisição HTTP com curl google.com](https://github.com/user-attachments/assets/8b2a421a-d835-4fa6-91f8-848fa245c3e5)

---

## 📌 Resumo dos comandos

| Comando     | Função                                           |
| ----------- | ------------------------------------------------ |
| `ip a`      | Exibe interfaces de rede e endereços IP          |
| `ip r`      | Exibe a tabela de rotas e o gateway padrão       |
| `ping`      | Testa a conectividade utilizando ICMP            |
| `ss -tulnp` | Exibe conexões e portas de rede em escuta        |
| `curl`      | Realiza requisições e testes de comunicação HTTP |

---

## 💡 Conceitos praticados

* Interfaces de rede;
* Endereçamento IPv4 e IPv6;
* Endereço MAC;
* Loopback;
* Tabela de roteamento;
* Gateway padrão;
* Protocolo ICMP;
* Testes de conectividade;
* Portas e serviços de rede;
* Protocolos TCP e UDP;
* Portas em estado de escuta (*LISTEN*);
* Requisições HTTP;
* Troubleshooting básico de redes.

---

## 🎓 Aplicação prática

Os conhecimentos praticados nesta etapa são aplicáveis a atividades de suporte técnico e infraestrutura, principalmente durante diagnósticos de problemas relacionados à conectividade, configuração de interfaces, roteamento e disponibilidade de serviços.

A utilização desses comandos permite realizar uma análise inicial do ambiente antes de investigar problemas mais complexos de rede.
