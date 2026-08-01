# 💾 Memória e Armazenamento

Nesta etapa foram praticados comandos para analisar o uso de espaço em disco, verificar o tamanho ocupado por diretórios e identificar dispositivos, partições e sistemas de arquivos montados no Linux.

Esses comandos são úteis em atividades de administração e troubleshooting, principalmente para identificar falta de espaço, analisar dispositivos de armazenamento e verificar sistemas de arquivos montados.

---

## 📊 `df -h` — Verificar espaço em disco

O comando `df -h` (*Disk Free*) exibe informações sobre o espaço utilizado e disponível nos sistemas de arquivos montados.

```bash
df -h
```

A opção `-h` (*human-readable*) apresenta os valores em unidades mais fáceis de interpretar.

Entre as informações apresentadas estão:

* Tamanho total do sistema de arquivos;
* Espaço utilizado;
* Espaço disponível;
* Percentual de utilização;
* Ponto de montagem.

Esse comando é útil para verificar rapidamente a utilização das partições e identificar sistemas de arquivos próximos de atingir sua capacidade máxima.

---

## 🔲 `lsblk` — Listar dispositivos de armazenamento

O comando `lsblk` (*List Block Devices*) exibe os dispositivos de armazenamento disponíveis e suas respectivas partições.

```bash
lsblk
```

A saída permite visualizar informações como:

* Discos disponíveis;
* Partições;
* Tamanho dos dispositivos;
* Estrutura hierárquica dos dispositivos;
* Pontos de montagem associados.

Esse comando é útil para identificar os dispositivos de armazenamento presentes no sistema e entender sua organização.

---

## 📸 Evidência prática — `df -h` e `lsblk`

O print abaixo apresenta a execução dos comandos `df -h` e `lsblk` durante a atividade prática, permitindo visualizar o espaço utilizado no sistema e os dispositivos de armazenamento disponíveis.

![Análise de espaço em disco e dispositivos de armazenamento](https://github.com/user-attachments/assets/0373edf7-d61a-44aa-b543-fc687ee1f0fe)

---

## 📁 `du -sh` — Verificar tamanho de diretórios

O comando `du` (*Disk Usage*) permite verificar quanto espaço está sendo utilizado por arquivos e diretórios.

```bash
du -sh
```

As opções utilizadas significam:

* `-s` — apresenta apenas o total do diretório analisado;
* `-h` — apresenta os valores em formato legível.

Esse comando é útil para identificar o espaço ocupado por um diretório e auxiliar na investigação de consumo de armazenamento.

---

## 🔗 `mount` — Verificar sistemas de arquivos montados

O comando `mount` permite visualizar os sistemas de arquivos atualmente montados no sistema.

```bash
mount
```

A saída apresenta informações sobre os dispositivos, sistemas de arquivos e respectivos pontos de montagem.

Esse comando pode ser utilizado para verificar se dispositivos e sistemas de arquivos estão montados corretamente e entender como estão integrados à estrutura de diretórios do Linux.

Durante a prática, foram realizadas duas verificações do comando `mount`, permitindo observar o estado dos sistemas de arquivos montados em momentos diferentes da atividade.

---

### 📸 Evidência inicial

O primeiro registro apresenta a execução inicial do comando `mount` durante a atividade prática.

![Verificação inicial dos sistemas de arquivos montados](https://github.com/user-attachments/assets/28b771a5-b662-497d-9afe-514d80b71cec)

---

### 📸 Evidência final

O segundo registro apresenta uma nova execução do comando `mount` ao final da atividade, permitindo comparar o estado dos sistemas de arquivos montados.

![Verificação final dos sistemas de arquivos montados](https://github.com/user-attachments/assets/ac72434e-56d5-40aa-90c3-e9f63ac6ba1b)

---

## 📌 Resumo dos comandos

| Comando  | Função                                                         |
| -------- | -------------------------------------------------------------- |
| `df -h`  | Exibe o espaço utilizado e disponível nos sistemas de arquivos |
| `lsblk`  | Lista discos, partições e dispositivos de armazenamento        |
| `du -sh` | Exibe o espaço ocupado pelo diretório analisado                |
| `mount`  | Exibe os sistemas de arquivos atualmente montados              |

---

## 💡 Conceitos praticados

* Análise de espaço disponível e utilizado em disco;
* Sistemas de arquivos;
* Discos e partições;
* Dispositivos de armazenamento;
* Pontos de montagem;
* Verificação de sistemas de arquivos montados;
* Uso do formato *human-readable*;
* Troubleshooting básico de armazenamento.
