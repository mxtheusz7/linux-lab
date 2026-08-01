# ⚙️ Processos e Recursos

Nesta etapa foram praticados comandos para visualizar, monitorar e gerenciar processos em execução, além de analisar o uso de memória e recursos do sistema Linux.

O monitoramento de processos é uma atividade importante em administração de sistemas e troubleshooting, permitindo identificar aplicações em execução, consumo de recursos e processos que podem precisar ser encerrados.

---

## 📋 `ps aux` — Listar processos

O comando `ps aux` exibe uma lista detalhada dos processos atualmente em execução no sistema.

```bash
ps aux
```

A saída apresenta informações como:

* Usuário responsável pelo processo;
* PID (*Process ID*);
* Uso de CPU;
* Uso de memória;
* Tempo de execução;
* Comando responsável pelo processo.

Esse comando é útil para realizar uma análise pontual dos processos ativos no sistema.

### 📸 Evidência prática

![Execução do comando ps aux](https://github.com/user-attachments/assets/33bea9aa-c93e-4831-8c99-9a159ad86ebd)

---

## 📊 `top` — Monitorar processos em tempo real

O comando `top` apresenta uma visão dinâmica dos processos e dos recursos utilizados pelo sistema.

```bash
top
```

A ferramenta permite acompanhar informações como:

* Uso da CPU;
* Memória RAM;
* Processos em execução;
* PID dos processos;
* Usuário responsável;
* Consumo individual de recursos.

Diferentemente do `ps aux`, que apresenta uma fotografia dos processos no momento da execução, o `top` atualiza as informações continuamente.

### 📸 Evidência prática

![Monitoramento de processos com top](https://github.com/user-attachments/assets/258b490f-ead0-4426-8304-fe85cb979ec4)

---

## 📈 `htop` — Monitoramento interativo

O `htop` é uma alternativa interativa ao `top`, apresentando informações de processos e recursos de forma mais visual.

```bash
htop
```

A ferramenta permite visualizar e organizar processos, além de facilitar a identificação do consumo de CPU e memória.

### 📸 Evidência prática

![Monitoramento de processos com htop](https://github.com/user-attachments/assets/c8d150ce-21e4-4fdc-b3a7-02f6a64b931d)

---

## ⏳ `sleep 300 &` — Executar processo em segundo plano

O comando `sleep` pausa a execução durante um período determinado. Ao utilizar `&` no final, o processo é executado em segundo plano (*background*).

```bash
sleep 300 &
```

Nesse exemplo, foi criado um processo que permaneceria ativo durante 300 segundos.

O terminal exibiu o PID do processo, que posteriormente foi utilizado para identificá-lo e encerrá-lo.

Para localizar o processo, foi utilizado:

```bash
ps aux | grep sleep
```

O processo foi encerrado utilizando o comando `kill` seguido do seu PID:

```bash
kill 6917
```

Após o encerramento, o processo foi novamente verificado para confirmar que não estava mais em execução.

### 📸 Evidência prática

![Execução e encerramento de processo em segundo plano](https://github.com/user-attachments/assets/4579d718-ba9b-4579-8da4-e8924e78fbc2)

---

## 🧠 `free -h` — Verificar memória

O comando `free -h` exibe informações sobre o uso da memória RAM e da área de Swap.

```bash
free -h
```

A opção `-h` (*human-readable*) apresenta os valores em unidades mais fáceis de interpretar, como MiB e GiB.

As informações apresentadas incluem:

* Memória total;
* Memória utilizada;
* Memória livre;
* Memória compartilhada;
* Memória em cache;
* Memória disponível;
* Uso de Swap.

### 📸 Evidência prática

![Uso de memória RAM e Swap com free -h](https://github.com/user-attachments/assets/60e6c282-50c5-4a32-8c06-9d07ac72a61b)

---

## 📌 Resumo dos comandos

| Comando                | Função                                             |
| ---------------------- | -------------------------------------------------- |
| `ps aux`               | Lista detalhadamente os processos em execução      |
| `top`                  | Monitora processos e recursos em tempo real        |
| `htop`                 | Monitora processos de forma interativa e visual    |
| `sleep 300 &`          | Executa um processo de espera em segundo plano     |
| `ps aux \| grep sleep` | Localiza processos relacionados ao comando `sleep` |
| `kill`                 | Encerra um processo utilizando seu PID             |
| `free -h`              | Exibe o uso de memória RAM e Swap                  |

---

## 💡 Conceitos praticados

* Processos e PID (*Process ID*);
* Monitoramento de processos;
* Uso de CPU e memória;
* Execução de processos em segundo plano (*background*);
* Identificação de processos;
* Encerramento de processos com `kill`;
* Monitoramento de memória RAM;
* Área de Swap;
* Troubleshooting básico de processos e recursos.
