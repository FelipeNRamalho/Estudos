# FASE 0 — FUNDAMENTOS DE COMPUTAÇÃO

Antes de falar de cloud, Kubernetes ou Riot, você precisa entender o que um sistema é de verdade.

# Objetivo da fase

Construir o alicerce mental:

* o que é um programa
* como o sistema operacional conversa com o hardware
* como processos, memória, disco e rede se relacionam
* como aplicações se comunicam

---

## 0.1 — Entender como um computador executa software

## Aprender:

* o que é **CPU**
* o que é **RAM**
* o que é **armazenamento**
* o que é **processo**
* o que é **thread**
* o que é **kernel**
* o que é **syscall**
* diferença entre **user space** e **kernel space**
* o que é **filesystem**
* o que é **socket**

## Você deve conseguir explicar:

* quando você executa `./app`, o que acontece?
* o que significa um processo “estar rodando”?
* o que é PID?
* por que memória e CPU viram gargalo?
* o que é um processo bloqueado em I/O?

---

## 0.2 — Sistema operacional: visão prática

## Aprender:

* o que o SO faz
* agendamento de processos
* memória virtual
* paginação
* file descriptors
* stdin / stdout / stderr
* permissões
* variáveis de ambiente
* sinais (`SIGTERM`, `SIGKILL`, etc.)

## Conceitos essenciais:

* processo vs thread
* foreground vs background
* daemon
* init/systemd
* exit code
* pipe
* redirecionamento de saída

---

## 0.3 — Representação de dados

## Aprender:

* bits, bytes
* binário, decimal, hexadecimal
* encoding de texto
* UTF-8
* JSON, YAML, TOML
* serialização e desserialização

---

## 0.4 — Estruturas de dados e complexidade

Você não vai virar pesquisador de algoritmos, mas precisa de base suficiente para programar e raciocinar bem.

## Aprender:

* arrays / slices
* listas
* mapas / hash tables
* pilhas
* filas
* árvores
* heaps
* grafos
* complexidade de tempo e espaço
* Big O

## Saber usar:

* busca linear e binária
* ordenação
* map/filter/reduce mentalmente, mesmo se a linguagem não usar esses nomes
* tabelas hash para lookup rápido

---

## Entregáveis da Fase 0

No fim da fase 0, você deve conseguir responder:

* o que é um processo?
* o que é um socket?
* o que é memória virtual?
* por que uma aplicação pode consumir muita RAM?
* qual a diferença entre CPU-bound e I/O-bound?
* o que significa latência de disco, rede e CPU?
