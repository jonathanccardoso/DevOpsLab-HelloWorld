# DevOps Essentials
Apresentations of general knowledge about devops.

## O que é
Combinações de praticas e ferramentas que aumentam a capacidade de uma empresa para distribuir aplicativos.
Alinhamentos dos times de desenvolvimento e operação englobando processos, ferramentas e responsabilidade.

DevOps -> desenvolvimento + operações
(melhores praticas p/ colaboração e comunicação)

Começou a partir do 'manifesto agile', conectando melhoradas e constantes aos clientes

## Pilares
cultura - colaboração
automatização - ferramentas de automatização e pipelines automáticas
medição - monitoração, metricas de todo o ciclo
compartilhamento - feedback, compartilhar responsabilidades

## Caracteristicas
-dev
desenvolvimento agil
diminuição na complexidade do sorftware
entrega continua
-ops
gerencia de configuração
monitoração e coleta de metricas
ambiente automatizado

## Beneficios
melhor comunicação e colaboração entre as areas
melhor qualidade e frequencia de entregas
maior estabilidade e melhor desemprenho
aumento do valor do negócio

## Metodologias Ageis
- scrum -> gestão de projetos, projetos fragmentados em sprints,
o mais importante é feito primeiro, prioridades(backlogs)
- kanban -> atividades do dia e status de cada area

** elementos do eixo/pilar Automação do movimento DevOps.
Deploy, controle, monitoração, gerência de configuração
e orquestração

(2)
## terminologias
-ops
infraestrutura agil e como codigo
gerencia de configuração
provisionameento automatico (containers,...)

-dev
desenvolvimento agil (manifesto agil)
integração, entrega continua
implantação continua

## PipeLine de desenvolvimento
-integração continua
o codigo é diretamente testado (de forma automatizada)
antes de por em produção.
-entrega continua
garantir versiões novas e ou atualizadas p/ entregar.
-implantação continua
depois do codigo "pronto" e feitos os testes o
codigo (a funcionabilidade) entra em produção.

- foco do pipeline de desenvolvimento
entrega da relesase de Software confiável para entrar
em produção

## pipeline DevOps = "um pipeline de pipelines"
(abrange muito mais coisa - "a união")
- foco na função das equipes
- automatização de teste para testes e segurança
- automação para operações
- aprovação para gerentes de lançamentos

** ajudando na automatizar e dimensionar fluxos
de trabalhos, p/ entrega continua.

(3)
Devops é inevitável no mercado, não somente na area de TI
Certificações em Devops é importante nessa area, pois são
mais bem empregados.
há muitas certficações no mercado, principais:
- na  it.certs_ o exame é gratuito mas o certificado é pago
- linux profession insstitute
- xin
- redhat
- amazon
- devops essencials
- devops master- dev e ops
- devops tools enginners (lpi)
- devops master (exin)
- devops essential (it certs)

(4)
## Relação do DevOps com o open source
- devops nao é ferramenta
- ferramenta é as automações feitas a partir dessa
filosofia
- devops e open source estão juntos

= usam configurações de ferramentas
- ansible, chef, puppet, terraform salt
- usam ferramentas de container
docker, amazon ecs/eks, kubernetes

## principais ferramentas DevOps
= ciclo devops (pipeline devops) - tools (free e comunicáveis):
(ok) - usados pelo 4linux, colocam dentro dos servidores essas plataformas

planejamento (planning collaborate),
- (plano) jira, redmine, trello, wekan, kanbanflow(ok)
- (comunicação) slack (com varias comunicações(ok)), rocket.chat(ok)
codigo (code),
- (IDE) visual studio code, atom, pycharm
- (SCM) github, gitlab(ok) e bitbucket
construção (build)-automatização em fazer o  deploy,
- (CI) jenkings, gitlab CI(ok), travis CI  
- (BUILD - pacote p/ artefatos) apache ant, grunt
testes (tests)-(integração continua)apos o commit fazemos os testes para nao quebrar o codigo,
- (tests) sonarqube(ok), phpunit (test php), pytest, se selenion(ok)
(entregando uma realease p/ colocar no repositorio)
deploy,
- nexus, dockerHUB
operação (operate),
- puppet, chef, ansible, docker
- heroku, azure, aws
- (management platfoorm) manage IQ, foreman
moitoração (monitor)
* soluções tem que estarem ligadas aos canaiss para envio de alertas p/ os times se mobilizarem
- prometheus, graylog, grafana
- kibana, elastic, splunk

= ferramentas de Gerência de Configuração: puppet, ansible
= ferramentas que atuam como um repositório e mantêm um histórico de todas as mudanças feitas no seu sistema: sistemas de controle de versoes
= Ferramentas da fase de monitoração: prometheus, zabbix

## Laboratório DevOps

= conhecer 4 plataformas:github, travis-CI, heroku e codeAnywhere
= comandos git
= criar uma pipeline devops

-ciclo devops
planejamento, codigo, construção,testes,deploy, operação, moitoração

#planning collasborate
1 - criar conta no codeanywhere, travis e no heroku
2 - no github em project podemos criar um planejamento kanban
 - github/4linux/devops-lab-hello-world
#code
3 - criando um repositorio no 'codeanywhere' e publicando
no 'github'
#build
4 - 'travis' configurar para aplicação e tests (com a biblioteca uniteTeste)
#test
5 - 'travis' - sync na conta github e add projeto
 - habilitar p/ a cada fez q tiver alteração ele fazer um deploy
 - 'status do deploy' status image - markdown - e copiar texto abaixo
 - para o 'travis' funcionar tem que ter o arquivo travis.yml (para configurações dos processos e testes) e o test.py
 - no 'travis' o projeto aparece um build dizendo se passou ou nao a alteração
#deploy e #operate
6 - usar o heroku
 - criar uma app no heroku e copiar a api key da sua conta
 - no projeto em settings criar uma variavel 'HEROKU_API_KEY' e colar a API_KEY
 - o mesmo nome da variavel exisstente em .travis.yml
 - e colocando o nome do proejto no heroku em .travis.yml em 'deploy' - 'app'
#monitor
7 - no heroku faz as monitorações que sao as 'metricas' em app no heroku
 - mostrando tempo de resposta da pagina
