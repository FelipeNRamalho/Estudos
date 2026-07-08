
# ROADMAP COMPLETO — INFRA / PLATFORM / SRE COM GO

## Objetivo final do roadmap

Ao terminar essa trilha, você deve ser capaz de:

* usar **Linux** com segurança e autonomia
* entender **redes** de verdade, não só decorar camadas
* programar bem em **Go**
* entender **Git** e fluxo de engenharia
* construir **APIs e serviços backend**
* modelar dados e operar **bancos relacionais e NoSQL**
* empacotar aplicações com **Docker**
* orquestrar workloads com **Kubernetes**
* provisionar infraestrutura com **Terraform**
* trabalhar com **cloud** (AWS preferencialmente)
* montar **CI/CD**
* operar sistemas com **observabilidade, SRE e troubleshooting**
* entender **sistemas distribuídos**
* construir uma **plataforma de microservices** séria, com cara de produção

---

# COMO USAR ESTE ROADMAP

A ordem recomendada é esta:

1. **Fundamentos de computação e terminal**
2. **Linux**
3. **Redes**
4. **Git**
5. **Programação sólida**
6. **Go**
7. **Backend e APIs**
8. **Banco de dados**
9. **Docker**
10. **Kubernetes**
11. **Cloud**
12. **Terraform / IaC**
13. **CI/CD**
14. **Observabilidade**
15. **SRE / operação**
16. **Sistemas distribuídos**
17. **Segurança de plataforma**
18. **Projeto final estilo Riot**
19. **Preparação para entrevistas**

Você **não precisa correr**. O ideal é fazer por blocos e só subir quando a base anterior estiver firme.

---

# VISÃO GERAL DA TRILHA

## Fase 0 — Fundamentos de computação

## Fase 1 — Linux e terminal

## Fase 2 — Redes e comunicação entre sistemas

## Fase 3 — Git e fluxo de desenvolvimento

## Fase 4 — Programação e algoritmos

## Fase 5 — Go do básico ao avançado

## Fase 6 — Backend e APIs

## Fase 7 — Bancos de dados e cache

## Fase 8 — Docker e containers

## Fase 9 — Kubernetes

## Fase 10 — Cloud (AWS)

## Fase 11 — Infra as Code com Terraform

## Fase 12 — CI/CD e automação

## Fase 13 — Observabilidade

## Fase 14 — SRE, incidentes e confiabilidade

## Fase 15 — Sistemas distribuídos

## Fase 16 — Segurança de plataforma

## Fase 17 — Projeto de plataforma completo

## Fase 18 — Currículo, GitHub e entrevistas

Agora vou abrir **cada fase em profundidade**.

---

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

---

# FASE 1 — LINUX E TERMINAL

Se você quer Infra, Linux deixa de ser “um sistema operacional” e vira **seu ambiente natural de trabalho**.

# Objetivo da fase

Sair do nível “sei rodar `ls` e `cd`” e chegar no nível:

* navegar com fluidez
* inspecionar processos
* ler logs
* gerenciar arquivos
* entender permissões
* instalar serviços
* diagnosticar problemas básicos

---

# 1.1 — Navegação e manipulação de arquivos

## Aprender:

* `pwd`
* `ls`, `ls -la`
* `cd`
* `mkdir`, `mkdir -p`
* `touch`
* `cp`
* `mv`
* `rm`, `rm -rf`
* `cat`
* `less`
* `head`, `tail`
* `find`
* `locate`
* `du`
* `df`

## Entender:

* caminhos absolutos e relativos
* diretórios especiais: `.`, `..`, `~`
* estrutura típica do Linux:

  * `/`
  * `/home`
  * `/etc`
  * `/var`
  * `/tmp`
  * `/usr`
  * `/bin`
  * `/sbin`
  * `/opt`

---

# 1.2 — Shell, pipes e redirecionamento

## Aprender:

* o que é shell
* bash/zsh
* pipes: `|`
* redirecionamento:

  * `>`
  * `>>`
  * `2>`
  * `2>&1`

## Comandos essenciais:

* `grep`
* `cut`
* `sort`
* `uniq`
* `wc`
* `xargs`
* `sed`
* `awk` (ao menos o básico)

## Saber fazer:

* filtrar logs
* contar linhas
* buscar texto em arquivos
* encadear comandos
* extrair colunas
* gerar relatórios simples pelo terminal

Exemplo de raciocínio:

```bash
cat app.log | grep ERROR | wc -l
```

---

# 1.3 — Usuários, grupos e permissões

## Aprender:

* `chmod`
* `chown`
* `chgrp`
* permissões `rwx`
* usuário, grupo, outros
* `sudo`
* UID/GID
* `umask`

## Entender:

* por que um processo pode tomar “permission denied”
* por que um serviço não consegue ler um arquivo
* o que é dono de um arquivo

---

# 1.4 — Processos e monitoramento

## Aprender:

* `ps`
* `top` / `htop`
* `pgrep`
* `kill`
* `kill -9`
* `jobs`, `bg`, `fg`
* `nohup`

## Entender:

* estado de processo
* CPU%
* MEM%
* RSS vs VIRT
* zombie process
* signal handling

---

# 1.5 — Rede no Linux

## Aprender:

* `ip addr`
* `ip route`
* `ss`
* `netstat` (conceitualmente)
* `curl`
* `wget`
* `ping`
* `traceroute`
* `dig` / `nslookup`

## Saber fazer:

* descobrir IP da máquina
* ver portas abertas
* testar endpoint HTTP
* resolver DNS
* identificar se um serviço está ouvindo em determinada porta

---

# 1.6 — Logs e systemd

## Aprender:

* o que é **systemd**
* o que é um **service unit**
* `systemctl status`
* `systemctl start/stop/restart`
* `journalctl`

## Entender:

* como um serviço sobe no boot
* onde olhar logs de serviço
* por que um serviço caiu

---

# 1.7 — Pacotes e ambiente

## Aprender:

* `apt`, `dnf` ou equivalente
* variáveis de ambiente
* `.bashrc`, `.profile`
* `PATH`

---

# Projeto da Fase 1

Monte uma VM Linux ou use WSL e faça:

## Projeto: “Administração básica de um servidor Linux”

* criar usuários e grupos
* criar diretórios com permissões específicas
* instalar Nginx
* subir uma página HTML simples
* consultar logs do Nginx
* reiniciar o serviço
* criar um script bash que:

  * verifica se o Nginx está ativo
  * registra resultado em um log
  * mostra uso de disco

---

# FASE 2 — REDES E COMUNICAÇÃO ENTRE SISTEMAS

Infra sem rede é impossível. Kubernetes, cloud, APIs, bancos, observabilidade — tudo passa por rede.

# Objetivo da fase

Entender como máquinas e serviços se comunicam.

---

# 2.1 — Base de redes

## Aprender:

* o que é rede
* LAN / WAN
* IP
* porta
* protocolo
* pacote
* roteamento
* NAT
* firewall

---

# 2.2 — Modelo TCP/IP e OSI

Não precisa decorar as 7 camadas como mantra. Precisa entender **quem faz o quê**.

## Aprender:

* aplicação
* transporte
* internet/rede
* enlace
* onde entram:

  * HTTP
  * DNS
  * TCP
  * UDP
  * IP
  * TLS

---

# 2.3 — IP, sub-rede e roteamento

## Aprender:

* IPv4
* máscara CIDR
* subnets
* gateway
* rota padrão
* tabela de roteamento
* rede privada vs pública

## Saber:

* interpretar `192.168.1.0/24`
* entender por que duas máquinas não se enxergam
* entender o papel do gateway

---

# 2.4 — TCP e UDP

## Aprender:

* handshake do TCP
* confiabilidade
* retransmissão
* ordenação
* controle de fluxo
* connection-oriented vs connectionless

## Entender:

* por que HTTP normalmente usa TCP
* quando UDP faz sentido
* o que significa timeout, retransmit, packet loss

---

# 2.5 — DNS

## Aprender:

* o que é DNS
* resolução de nome
* A, AAAA, CNAME, MX, TXT
* TTL
* cache de DNS

## Saber:

* usar `dig`
* diagnosticar resolução quebrada

---

# 2.6 — HTTP e HTTPS

## Aprender:

* request / response
* método GET, POST, PUT, DELETE
* status codes
* headers
* body
* cookies
* autenticação por token
* keep-alive
* timeout
* idempotência

## HTTPS / TLS

* handshake TLS
* certificado
* CA
* por que HTTPS existe

---

# 2.7 — Load balancing e proxies

## Aprender:

* reverse proxy
* load balancer L4 vs L7
* sticky session
* health checks
* rate limiting

---

# Projeto da Fase 2

## Projeto: “Diagnóstico de rede e API”

* subir uma API simples localmente
* usar `curl` para testar endpoints
* inspecionar portas com `ss -tulpn`
* usar `dig` para consultar DNS de alguns domínios
* documentar:

  * IP local
  * gateway
  * DNS configurado
  * portas abertas
  * fluxo de uma requisição HTTP até chegar ao servidor

---

# FASE 3 — GIT E FLUXO DE DESENVOLVIMENTO

Infra e platform engineering trabalham com código o tempo todo.

# Objetivo da fase

Controlar versões, colaborar e manter histórico limpo.

---

# 3.1 — Fundamentos do Git

## Aprender:

* repositório
* working directory
* staging area
* commit
* branch
* merge

## Comandos:

* `git init`
* `git status`
* `git add`
* `git commit`
* `git log`
* `git diff`
* `git branch`
* `git checkout` / `git switch`
* `git merge`

---

# 3.2 — Git remoto

## Aprender:

* `git clone`
* `git remote`
* `git fetch`
* `git pull`
* `git push`

## Entender:

* repositório local vs remoto
* upstream branch
* conflitos

---

# 3.3 — Fluxo avançado

## Aprender:

* `git rebase`
* squash
* cherry-pick
* reset
* revert
* stash
* tags

---

# 3.4 — Boas práticas

## Aprender:

* mensagens de commit claras
* branch por feature
* PR/MR
* revisão de código
* `.gitignore`

---

# Projeto da Fase 3

* criar um repositório de laboratório
* fazer branch de feature
* criar commits pequenos
* simular conflito e resolver
* praticar merge e rebase
* publicar no GitHub

---

# FASE 4 — PROGRAMAÇÃO E ALGORITMOS

Antes de especializar em Go, a sua base de programação precisa ser limpa.

# Objetivo da fase

Aprender a pensar como programador de sistemas:

* decompor problemas
* modelar dados
* escrever funções limpas
* testar
* depurar

---

# 4.1 — Lógica de programação

## Aprender:

* variáveis
* tipos
* condicionais
* loops
* funções
* arrays/listas
* mapas
* structs/objetos
* tratamento de erro

---

# 4.2 — Boas práticas de código

## Aprender:

* legibilidade
* nomes de variáveis
* funções pequenas
* separação de responsabilidades
* modularização

---

# 4.3 — Algoritmos básicos

## Aprender:

* busca linear
* busca binária
* ordenação
* pilha
* fila
* recursão básica
* mapas para contagem e lookup

---

# 4.4 — Debugging

## Aprender:

* prints estratégicos
* logs
* uso de debugger
* leitura de stack trace

---

# Exercícios da Fase 4

Implemente programas para:

* contar frequência de palavras
* validar parênteses balanceados
* fila de atendimento
* parser simples de arquivo CSV
* encontrar duplicados
* simular rate limiter simples

---

# FASE 5 — GO DO BÁSICO AO AVANÇADO

Agora começa a linguagem principal da trilha.

# Objetivo da fase

Sair de “sei sintaxe” para “consigo escrever serviços, ferramentas e automações em Go”.

---

# 5.1 — Go básico

## Aprender:

* instalação e ambiente
* `go mod`
* estrutura de projeto
* `package main`
* `func main()`
* variáveis
* tipos
* `if`, `for`, `switch`
* arrays, slices, maps
* funções
* múltiplos retornos

---

# 5.2 — Structs, métodos e interfaces

## Aprender:

* `struct`
* métodos
* receivers
* interfaces
* composição
* visibilidade de identificadores (maiúscula/minúscula)

---

# 5.3 — Erros em Go

## Aprender:

* `error`
* `fmt.Errorf`
* wrapping de erro
* tratamento explícito
* `errors.Is`
* `errors.As`

---

# 5.4 — Ponteiros e memória

## Aprender:

* ponteiros
* passagem por valor
* referência prática em Go
* quando usar ponteiro em struct/método

---

# 5.5 — Pacotes essenciais da stdlib

## Estudar:

* `fmt`
* `os`
* `io`
* `bufio`
* `strings`
* `strconv`
* `time`
* `context`
* `sync`
* `net/http`
* `encoding/json`
* `log` / `slog`

---

# 5.6 — Concorrência em Go

Essa é uma parte central se você quer infra.

## Aprender:

* goroutines
* channels
* buffered vs unbuffered channels
* `select`
* worker pools
* cancellation
* timeouts
* `sync.Mutex`
* `sync.WaitGroup`
* `context.Context`

## Você deve conseguir:

* paralelizar tarefas
* cancelar processamento
* evitar race conditions
* controlar concorrência

---

# 5.7 — Arquivos, CLI e automação

## Aprender:

* leitura e escrita de arquivo
* flags de linha de comando
* variáveis de ambiente
* execução de comandos externos
* parse de JSON/YAML
* logs estruturados

---

# 5.8 — HTTP em Go

## Aprender:

* criar servidor HTTP
* handlers
* middleware
* cliente HTTP
* timeouts
* serialização JSON
* validação de entrada

---

# 5.9 — Testes em Go

## Aprender:

* `go test`
* testes unitários
* table-driven tests
* benchmark básico
* mocking simples por interface

---

# 5.10 — Go avançado para infra

## Aprender:

* profiling com `pprof`
* race detector
* graceful shutdown
* retry com backoff
* idempotência
* design de worker/queue
* clientes gRPC/HTTP robustos

---

# Projetos da Fase 5

Você deve construir **todos** estes:

## Projeto 1 — CLI de inspeção de sistema

Ferramenta em Go que:

* lê uso de CPU/memória/disco
* lista processos
* exporta relatório JSON

## Projeto 2 — Log parser concorrente

* lê múltiplos arquivos de log
* processa em paralelo
* conta erros por tipo
* gera resumo

## Projeto 3 — API HTTP em Go

* CRUD simples
* validação
* logs
* middleware de autenticação fake
* persistência em banco

## Projeto 4 — Worker assíncrono

* fila simples
* goroutines
* retry
* timeout
* DLQ simulada

---

# FASE 6 — BACKEND E APIs

Infra forte precisa entender o que está operando. Então você precisa saber construir serviços backend de verdade.

# Objetivo da fase

Construir APIs e serviços com qualidade de produção.

---

# 6.1 — Arquitetura de backend

## Aprender:

* o que é API
* REST
* JSON
* autenticação
* autorização
* middleware
* camadas:

  * handler/controller
  * service
  * repository
  * domain/model

---

# 6.2 — API REST

## Aprender:

* GET, POST, PUT, PATCH, DELETE
* status codes corretos
* paginação
* filtros
* ordenação
* validação de input

---

# 6.3 — Design de serviço

## Aprender:

* separação por camadas
* config via env vars
* logs estruturados
* timeouts
* health checks
* graceful shutdown
* versionamento de API

---

# 6.4 — Autenticação e autorização

## Aprender:

* JWT conceitualmente
* session vs token
* RBAC básico
* API keys

---

# 6.5 — gRPC

Para infra e platform, vale muito.

## Aprender:

* protobuf
* service definitions
* unary RPC
* streaming conceitual
* gRPC vs REST

---

# Projeto da Fase 6

## Serviço de “Player Inventory API”

Crie uma API em Go com:

* cadastro de player
* inventário
* itens
* consumo de item
* logs estruturados
* autenticação simples
* health endpoint
* métricas básicas

---

# FASE 7 — BANCOS DE DADOS E CACHE

Você precisa saber persistir e consultar dados com responsabilidade.

# Objetivo da fase

Entender modelagem, consultas, índices e padrões de acesso.

---

# 7.1 — SQL e modelagem relacional

## Aprender:

* tabelas
* linhas
* colunas
* chave primária
* chave estrangeira
* normalização básica
* relacionamentos 1:1, 1:N, N:N

## SQL:

* `SELECT`
* `INSERT`
* `UPDATE`
* `DELETE`
* `JOIN`
* `GROUP BY`
* `ORDER BY`
* `LIMIT`
* `WHERE`

---

# 7.2 — Índices e performance

## Aprender:

* índice
* scan
* cardinalidade
* plano de execução conceitual
* por que query fica lenta

---

# 7.3 — Transações

## Aprender:

* ACID
* commit / rollback
* isolation level conceitual
* race condition de banco

---

# 7.4 — Redis / cache

## Aprender:

* cache key-value
* TTL
* cache hit/miss
* invalidação
* rate limiting simples com Redis
* fila simples

---

# 7.5 — Mensageria

## Aprender conceitualmente:

* fila
* pub/sub
* ack
* retry
* dead letter queue

Pode usar **RabbitMQ** ou estudar também **Kafka** em nível introdutório.

---

# Projeto da Fase 7

Expandir a API anterior com:

* Postgres
* migrations
* índices
* Redis para cache de inventário
* fila para processamento assíncrono de eventos

---

# FASE 8 — DOCKER E CONTAINERS

Agora você sai do “roda na minha máquina” para empacotamento de aplicação.

# Objetivo da fase

Entender como aplicações são empacotadas e executadas em containers.

---

# 8.1 — O que é container de verdade

## Aprender:

* container ≠ VM
* namespaces
* cgroups
* imagem
* camada
* registry
* processo PID 1 dentro do container

---

# 8.2 — Docker básico

## Aprender:

* `Dockerfile`
* `docker build`
* `docker run`
* `docker ps`
* `docker logs`
* `docker exec`
* `docker stop`
* `docker rm`
* `docker images`

---

# 8.3 — Dockerfile bem feito

## Aprender:

* imagem base
* multi-stage build
* minimizar tamanho
* copiar binário
* expor porta
* variáveis de ambiente
* entrypoint/cmd

---

# 8.4 — Docker Compose

## Aprender:

* subir app + banco + redis
* volumes
* redes
* dependências de serviço

---

# Projeto da Fase 8

Containerize a API completa:

* API Go
* Postgres
* Redis
* worker
* Nginx opcional como reverse proxy

Tudo subindo com Docker Compose.

---

# FASE 9 — KUBERNETES

Aqui começa a parte mais importante para infra moderna.

# Objetivo da fase

Entender Kubernetes como **plataforma de execução de workloads distribuídos**.

---

# 9.1 — Fundamentos do Kubernetes

## Aprender:

* cluster
* control plane
* node
* kubelet
* etcd
* scheduler
* API server

---

# 9.2 — Objetos básicos

## Aprender:

* Pod
* Deployment
* ReplicaSet
* Service
* ConfigMap
* Secret
* Namespace

---

# 9.3 — Operação de workloads

## Aprender:

* rollout
* rollback
* scaling
* probes:

  * liveness
  * readiness
  * startup
* requests/limits

---

# 9.4 — Networking no Kubernetes

## Aprender:

* ClusterIP
* NodePort
* LoadBalancer
* Ingress
* DNS interno
* service discovery

---

# 9.5 — Agendamento e resiliência

## Aprender:

* taints/tolerations
* affinity/anti-affinity
* pod disruption budget
* HPA
* autoscaling conceitual

---

# 9.6 — Storage

## Aprender:

* volume
* persistent volume
* persistent volume claim
* storage class

---

# 9.7 — Segurança no cluster

## Aprender:

* RBAC
* service accounts
* secrets
* network policies
* security context

---

# 9.8 — Helm e organização

## Aprender:

* charts
* values
* templates
* empacotamento de apps

---

# 9.9 — Troubleshooting em Kubernetes

## Aprender:

* `kubectl get`
* `kubectl describe`
* `kubectl logs`
* `kubectl exec`
* `kubectl port-forward`

## Saber diagnosticar:

* CrashLoopBackOff
* ImagePullBackOff
* OOMKilled
* readiness falhando
* serviço sem endpoint
* DNS interno falhando

---

# Projeto da Fase 9

Suba sua plataforma em Kubernetes com:

* API
* worker
* Postgres ou banco gerenciado fake/local
* Redis
* Ingress
* HPA
* ConfigMap/Secret
* probes
* namespace separado

Idealmente use **kind**, **minikube** ou **k3d** no começo.

---

# FASE 10 — CLOUD (AWS)

Se o foco é empregabilidade em infra, AWS é o melhor primeiro alvo.

# Objetivo da fase

Entender cloud como ambiente operacional real.

---

# 10.1 — Fundamentos de cloud

## Aprender:

* IaaS / PaaS / SaaS
* região / zona
* elasticidade
* escalabilidade vertical e horizontal
* custo e billing

---

# 10.2 — Networking na AWS

## Aprender:

* VPC
* subnet pública e privada
* route table
* internet gateway
* NAT gateway
* security groups
* NACL

---

# 10.3 — Compute

## Aprender:

* EC2
* autoscaling group
* load balancer
* user data

---

# 10.4 — Containers na AWS

## Aprender:

* ECR
* ECS conceitualmente
* EKS com mais profundidade se o foco for Kubernetes

---

# 10.5 — Banco e storage

## Aprender:

* RDS
* S3
* ElastiCache conceitualmente

---

# 10.6 — IAM

## Aprender:

* usuário, role, policy
* least privilege
* credenciais temporárias

---

# 10.7 — Observabilidade na AWS

## Aprender:

* CloudWatch
* logs
* métricas
* alarmes

---

# Projeto da Fase 10

Suba um ambiente na AWS com:

* VPC
* subnets
* EC2
* banco
* aplicação containerizada
* load balancer
* monitoramento básico

Se quiser focar mais em Riot-style infra, o ideal é caminhar para **EKS**.

---

# FASE 11 — TERRAFORM / INFRA AS CODE

Agora a infraestrutura deixa de ser “clique no console” e vira código versionado.

# Objetivo da fase

Provisionar infraestrutura de forma reproduzível, auditável e escalável.

---

# 11.1 — Fundamentos do Terraform

## Aprender:

* providers
* resources
* variables
* outputs
* state
* plan / apply / destroy

---

# 11.2 — Estruturação séria

## Aprender:

* módulos
* separação por ambiente
* remote state
* state locking
* convenções de naming
* outputs compartilhados

---

# 11.3 — Terraform + AWS

## Aprender a provisionar:

* VPC
* subnets
* security groups
* EC2
* RDS
* IAM
* EKS conceitualmente ou com prática depois

---

# 11.4 — Integração com pipelines

## Aprender:

* validar Terraform em CI
* `fmt`, `validate`, `plan`
* revisão de mudanças de infra

---

# Projeto da Fase 11

Escrever a infraestrutura da sua plataforma inteira em Terraform:

* rede
* compute ou EKS
* storage
* banco
* IAM básico
* observabilidade mínima

---

# FASE 12 — CI/CD E AUTOMAÇÃO

Infra de alto nível constrói **plataformas de entrega**.

# Objetivo da fase

Automatizar build, teste, empacotamento e deploy.

---

# 12.1 — Conceitos

## Aprender:

* CI
* CD
* pipeline
* artefato
* versionamento
* promoção entre ambientes

---

# 12.2 — GitHub Actions ou GitLab CI

## Aprender:

* workflow
* jobs
* steps
* runners
* secrets

---

# 12.3 — Pipeline da aplicação

## Pipeline mínimo:

* lint
* testes
* build
* imagem Docker
* push para registry
* deploy

---

# 12.4 — Estratégias de deploy

## Aprender:

* rolling update
* blue/green
* canary

---

# 12.5 — GitOps

## Aprender conceitualmente:

* ArgoCD / Flux
* repositório declarativo
* desired state

---

# Projeto da Fase 12

Pipeline completo para sua plataforma:

* push no GitHub
* roda testes Go
* builda imagem
* publica em registry
* atualiza deployment no cluster
* executa smoke test

---

# FASE 13 — OBSERVABILIDADE

Sem observabilidade você não opera nada com segurança.

# Objetivo da fase

Conseguir responder:

* o sistema está saudável?
* onde está o gargalo?
* qual serviço está falhando?
* o deploy piorou a latência?

---

# 13.1 — Logs

## Aprender:

* logs estruturados
* correlação por request ID
* níveis de log
* evitar logs inúteis

---

# 13.2 — Métricas

## Aprender:

* counter
* gauge
* histogram
* summary conceitual
* p50/p95/p99
* taxa de erro
* throughput

---

# 13.3 — Tracing

## Aprender:

* trace
* span
* contexto distribuído
* correlação entre serviços

---

# 13.4 — Stack de observabilidade

## Estudar:

* Prometheus
* Grafana
* OpenTelemetry
* Loki ou outra solução de logs

---

# 13.5 — SLI / SLO

## Aprender:

* disponibilidade
* latência
* taxa de erro
* error budget

---

# Projeto da Fase 13

Instrumente a plataforma:

* métricas por endpoint
* dashboard de latência/erros
* logs estruturados
* tracing entre API e worker
* alertas básicos

---

# FASE 14 — SRE, INCIDENTES E CONFIABILIDADE

Aqui você começa a pensar como operador de produção.

# Objetivo da fase

Aprender a manter sistemas vivos sob falha.

---

# 14.1 — Confiabilidade

## Aprender:

* SLA
* SLI
* SLO
* error budget
* toil
* runbook
* postmortem

---

# 14.2 — Resiliência de aplicação

## Aprender:

* retry
* exponential backoff
* circuit breaker
* timeout
* bulkhead
* fallback
* idempotência

---

# 14.3 — Gestão de incidentes

## Aprender:

* triagem
* mitigação
* rollback
* comunicação de incidente
* análise de causa raiz

---

# 14.4 — Capacity planning

## Aprender:

* throughput
* saturation
* gargalo de CPU
* gargalo de I/O
* carga e stress test

---

# Projeto da Fase 14

Simule incidentes:

* derrube o banco
* aumente latência artificialmente
* faça worker travar
* faça um deploy quebrado
* documente:

  * sintomas
  * métricas afetadas
  * mitigação
  * causa raiz
  * prevenção

---

# FASE 15 — SISTEMAS DISTRIBUÍDOS

Esse é um dos blocos que mais separa “bom operacional” de “engenheiro de plataforma forte”.

# Objetivo da fase

Entender o comportamento de sistemas compostos por múltiplos serviços e nós.

---

# 15.1 — Conceitos fundamentais

## Aprender:

* latência de rede
* partial failure
* consistência
* disponibilidade
* replicação
* particionamento
* filas e processamento assíncrono

---

# 15.2 — Padrões importantes

## Aprender:

* service discovery
* API gateway
* saga conceitual
* outbox pattern
* idempotência
* deduplicação
* event-driven architecture

---

# 15.3 — CAP e trade-offs

## Aprender:

* consistência vs disponibilidade em cenários distribuídos
* quando cache piora consistência
* quando retry duplica efeito colateral

---

# 15.4 — Comunicação síncrona e assíncrona

## Aprender:

* REST/gRPC
* fila
* pub/sub
* event bus
* backpressure

---

# Projeto da Fase 15

Transforme sua plataforma em um mini ecossistema distribuído:

* service A: player
* service B: inventory
* service C: match rewards
* worker de processamento
* Redis/cache
* fila de eventos
* tracing entre todos

---

# FASE 16 — SEGURANÇA DE PLATAFORMA

Infra forte precisa de higiene de segurança.

# Objetivo da fase

Entender segurança aplicada à operação e à plataforma.

---

# 16.1 — Identidade e acesso

## Aprender:

* princípio do menor privilégio
* IAM
* RBAC
* service accounts

---

# 16.2 — Segredos e credenciais

## Aprender:

* secret managers conceitualmente
* rotação de credenciais
* evitar segredo hardcoded
* variáveis de ambiente vs secret store

---

# 16.3 — Segurança de container e cluster

## Aprender:

* imagem mínima
* non-root containers
* scanning
* network policies
* policies de admissão conceitualmente

---

# 16.4 — Segurança de aplicação

## Aprender:

* validação de input
* rate limiting
* autenticação
* TLS
* proteção de endpoints administrativos

---

# Projeto da Fase 16

Endureça sua plataforma:

* remover segredos hardcoded
* rodar containers como non-root
* limitar acesso por RBAC
* criar policies básicas
* documentar riscos remanescentes

---

# FASE 17 — PROJETO FINAL ESTILO RIOT

Aqui você junta tudo.

# Objetivo da fase

Construir uma plataforma que demonstre competência em:

* backend
* infra
* automação
* confiabilidade
* observabilidade
* cloud
* Kubernetes
* Go

---

# Projeto final recomendado

## “Game Services Platform”

Uma plataforma de serviços online para jogo, com esta arquitetura:

### Serviços

* **player-service**
* **inventory-service**
* **match-service**
* **reward-service**
* **auth-service** simples
* **notification-worker**

### Infra

* Kubernetes
* Ingress
* Redis
* Postgres
* mensageria
* observabilidade
* CI/CD
* Terraform
* deploy automatizado

### Requisitos técnicos do projeto

## Backend

* APIs REST ou gRPC
* validação
* autenticação
* logs estruturados
* health checks
* graceful shutdown

## Distribuído

* comunicação entre serviços
* fila de eventos
* retries
* idempotência

## Kubernetes

* Deployments
* Services
* ConfigMaps
* Secrets
* HPA
* Ingress
* probes
* namespaces

## IaC

* Terraform para rede e recursos cloud
* módulos organizados

## CI/CD

* pipeline por serviço
* build + test + docker + deploy

## Observabilidade

* dashboards
* métricas
* tracing
* alertas

## Operação

* runbook
* postmortem simulado
* testes de carga
* troubleshooting guide

---

# COMO ESTRUTURAR O REPOSITÓRIO DO PROJETO FINAL

Você pode dividir em múltiplos repositórios ou monorepo. Para começar, monorepo é mais simples.

Exemplo:

```text
game-services-platform/
├─ services/
│  ├─ player-service/
│  ├─ inventory-service/
│  ├─ match-service/
│  ├─ reward-service/
│  └─ auth-service/
├─ workers/
│  └─ notification-worker/
├─ deploy/
│  ├─ docker/
│  ├─ kubernetes/
│  ├─ helm/
│  └─ terraform/
├─ observability/
│  ├─ dashboards/
│  ├─ alerts/
│  └─ tracing/
├─ docs/
│  ├─ architecture.md
│  ├─ runbooks/
│  ├─ incident-postmortems/
│  └─ diagrams/
└─ .github/workflows/
```

---

# FASE 18 — CURRÍCULO, GITHUB E ENTREVISTAS

Agora entra a camada de posicionamento profissional.

# Objetivo da fase

Traduzir conhecimento técnico em sinal claro de empregabilidade.

---

# 18.1 — GitHub

Seu GitHub deve mostrar:

* projetos reais
* commits consistentes
* README bom
* arquitetura explicada
* instruções de execução
* decisões técnicas

## O que cada projeto precisa ter:

* objetivo
* arquitetura
* stack
* como rodar
* endpoints
* dashboards ou prints
* incidentes simulados
* melhorias futuras

---

# 18.2 — Currículo

No currículo, destaque:

* Go
* Linux
* Docker
* Kubernetes
* AWS
* Terraform
* CI/CD
* observabilidade
* APIs/microservices
* troubleshooting / automação / reliability

---

# 18.3 — Tipos de entrevista para esse caminho

Você precisa se preparar para 5 blocos:

## 1. Linux / redes / troubleshooting

Exemplos:

* “o pod está em CrashLoopBackOff, como você investigaria?”
* “por que a API responde localmente mas não no cluster?”
* “o serviço está lento, o que você olha primeiro?”

## 2. Go / programação

* concorrência
* interfaces
* erros
* design de serviço
* testes

## 3. Kubernetes / cloud / Terraform

* deployment, service, ingress
* requests/limits
* IAM
* rede em VPC
* state do Terraform

## 4. System design

* desenhar plataforma de matchmaking, chat, inventory, auth, telemetry
* pensar em escalabilidade, cache, filas, consistência, observabilidade

## 5. SRE / operação

* SLI/SLO
* incidentes
* rollback
* runbooks
* alertas

---

# ORDEM EXATA DE EXECUÇÃO DO ROADMAP

Se você quer o **passo a passo operacional**, eu seguiria exatamente esta ordem:

# BLOCO 1 — BASE DE COMPUTAÇÃO

1. fundamentos de computador, processo, memória, syscall
2. filesystem, shell, encoding, JSON/YAML
3. estruturas de dados e Big O

# BLOCO 2 — LINUX

4. terminal e filesystem
5. permissões e usuários
6. processos, logs, systemd
7. rede no Linux
8. scripts bash básicos

# BLOCO 3 — REDES

9. TCP/IP, DNS, HTTP, TLS
10. subnet, roteamento, NAT, firewall
11. load balancer e reverse proxy

# BLOCO 4 — GIT

12. init, add, commit, branch, merge
13. clone, fetch, pull, push
14. rebase, reset, revert, stash

# BLOCO 5 — PROGRAMAÇÃO

15. lógica, funções, estruturas de dados
16. testes e debugging
17. pequenos programas utilitários

# BLOCO 6 — GO

18. sintaxe e módulos
19. structs, interfaces, erros
20. arquivos, JSON, HTTP
21. concorrência
22. testes
23. CLI e automação

# BLOCO 7 — BACKEND

24. REST
25. arquitetura em camadas
26. autenticação
27. health checks, logs, config
28. gRPC introdutório

# BLOCO 8 — DADOS

29. SQL e modelagem
30. índices e transações
31. Redis
32. mensageria introdutória

# BLOCO 9 — CONTAINERS

33. Docker e Dockerfile
34. Compose
35. empacotar sua aplicação

# BLOCO 10 — KUBERNETES

36. pods, deployments, services
37. configmaps, secrets, probes
38. ingress, HPA, RBAC
39. troubleshooting de cluster

# BLOCO 11 — CLOUD

40. VPC, subnet, SG, EC2, IAM
41. RDS, S3, observabilidade
42. EKS conceitual e depois prático

# BLOCO 12 — TERRAFORM

43. resources, variables, outputs, state
44. módulos e ambientes
45. provisionar AWS com Terraform

# BLOCO 13 — CI/CD

46. GitHub Actions
47. build/test/docker/deploy
48. rollout e smoke tests

# BLOCO 14 — OBSERVABILIDADE

49. logs estruturados
50. Prometheus/Grafana
51. tracing e SLOs

# BLOCO 15 — SRE

52. incidentes
53. runbooks
54. postmortem
55. capacity planning

# BLOCO 16 — DISTRIBUÍDO

56. filas, eventos, retries, idempotência
57. service-to-service communication
58. cache e consistência
59. desenho de sistemas

# BLOCO 17 — SEGURANÇA

60. IAM, RBAC, segredos
61. hardening de container
62. TLS e proteção de APIs

# BLOCO 18 — PROJETO FINAL

63. desenhar arquitetura
64. implementar serviços
65. containerizar
66. subir em Kubernetes
67. provisionar infra com Terraform
68. criar CI/CD
69. instrumentar observabilidade
70. simular incidentes
71. documentar tudo

---

# O QUE VOCÊ DEVE ESTUDAR EM PARALELO DURANTE TODA A TRILHA

Algumas coisas não são “uma fase só”; elas acompanham o roadmap inteiro.

## A) Inglês técnico

Você vai precisar ler:

* documentação
* RFCs
* artigos de engenharia
* vagas
* issues de GitHub

## B) Escrita técnica

Aprenda a escrever:

* README
* documentação de arquitetura
* postmortem
* runbook
* descrição de PR

## C) Troubleshooting

Sempre que estudar algo, pergunte:

* como isso quebra?
* como eu diagnostico?
* quais sintomas aparecem?
* quais métricas/logs eu olharia?

## D) Leitura de documentação oficial

Priorize docs de:

* Go
* Docker
* Kubernetes
* AWS
* Terraform
* Prometheus

---

# COMO SABER SE VOCÊ PODE PASSAR PARA A PRÓXIMA FASE

Use esta regra:

## Você pode avançar quando conseguir:

1. **explicar o conceito com suas palavras**
2. **usar o conceito na prática**
3. **diagnosticar um problema básico envolvendo aquele conceito**
4. **integrar o conceito com o que veio antes**

Exemplo:

* antes de sair de Docker para Kubernetes, você deve saber buildar imagem, rodar container, inspecionar logs, passar env vars, conectar com banco e entender o que está rodando dentro do container.

---

# O QUE EU FARIA NO SEU LUGAR, NA PRÁTICA

Se eu estivesse montando sua formação do zero com foco em **Infra + Riot + Go**, eu faria assim:

## Etapa 1

* Fase 0 inteira
* Fase 1 inteira
* Fase 2 inteira
* Fase 3 inteira

## Etapa 2

* Fase 4
* Fase 5 inteira em Go
* pequenos projetos utilitários

## Etapa 3

* Fase 6 e 7
* uma API séria com Postgres + Redis

## Etapa 4

* Fase 8 e 9
* colocar essa API em Docker e Kubernetes

## Etapa 5

* Fase 10, 11 e 12
* levar para AWS com Terraform e pipeline

## Etapa 6

* Fase 13, 14, 15 e 16
* transformar isso em plataforma observável e confiável

## Etapa 7

* Fase 17 e 18
* projeto final + GitHub + entrevistas

---

# RESULTADO ESPERADO NO FINAL

No final dessa trilha, o seu perfil ideal seria algo assim:

> “Engenheiro com base sólida em Linux, redes e programação; experiência prática em Go para serviços e automação; domínio de Docker, Kubernetes, AWS e Terraform; capacidade de construir e operar APIs e microservices com observabilidade, CI/CD e princípios de SRE; confortável com troubleshooting, reliability e arquitetura distribuída.”

Isso já conversa muito bem com vagas de:

* **Infrastructure Engineer**
* **Platform Engineer**
* **SRE**
* **Backend Engineer (services/platform)**
* **Cloud Engineer com foco em plataforma**
* **Developer Infrastructure**

---

# PRÓXIMO PASSO RECOMENDADO

O roadmap acima é o **mapa completo**. Agora o melhor movimento é transformar isso em **plano de execução**.

Eu posso fazer isso de duas formas:

## Opção 1 — transformar este roadmap em **módulos de estudo numerados**

Exemplo:

* **Módulo 1: Fundamentos de Linux**
* **Módulo 2: Redes para Infra**
* **Módulo 3: Go básico**
* etc.

E em cada módulo eu te entrego:

* ordem exata dos assuntos
* aula teórica
* exercícios
* mini projeto
* checklist de domínio

## Opção 2 — montar um **currículo completo estilo curso**, começando pela Aula 1

Aí eu viro seu instrutor e seguimos em sequência, por exemplo:

* **Curso Infra/Platform para Riot com Go**

  * Aula 1 — Como um computador executa um processo
  * Aula 2 — Linux: filesystem e shell
  * Aula 3 — Processos, memória e sinais
  * Aula 4 — Redes: IP, portas, DNS e HTTP
  * Aula 5 — Git na prática
  * Aula 6 — Go básico
  * ...
