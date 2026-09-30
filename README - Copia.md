# EscolaConecta

Plataforma web que centraliza a comunicação entre escola, professores e responsáveis, reduzindo a dependência de grupos de WhatsApp, bilhetes de papel e ligações.

## Problema

A comunicação entre escola e famílias é fragmentada: avisos, recados, calendário de provas, reuniões e comunicados importantes se espalham entre WhatsApp, bilhetes em papel e agenda escolar, e muitas vezes não chegam a quem precisa.

**Quem enfrenta o problema:** responsáveis (recebem tarde ou perdem avisos), professores e coordenação (repetem avisos em vários canais), alunos (esquecem de repassar recados).

**Dificuldades atuais:** mensagens perdidas em conversas paralelas, sem confirmação de leitura, bilhetes extraviados, informações desencontradas, uso do número pessoal do professor, sem histórico organizado.

## Solução

O EscolaConecta centraliza avisos, comunicados, datas de provas e convites para reuniões em um único canal oficial, direcionados para toda a escola, uma turma ou um aluno específico. Responsáveis recebem notificações e confirmam a leitura, e a escola acompanha quem já viu cada aviso. O histórico fica organizado e disponível para consulta.

**Objetivo geral:** garantir que informações importantes da escola cheguem às famílias de forma rápida, confiável e rastreável, reduzindo ruídos e retrabalho da equipe escolar.

## Público-alvo

- Responsáveis pelos alunos
- Professores
- Coordenação e direção
- Secretaria escolar
- Alunos (consulta de avisos e calendário)

## Requisitos funcionais

| ID | Descrição |
|----|-----------|
| RF01 | Autenticação com e-mail e senha, com perfis distintos (responsável, professor, coordenação, secretaria, aluno) |
| RF02 | Professores e coordenação publicam avisos e comunicados |
| RF03 | Direcionar um aviso para toda a escola, uma turma ou um aluno específico |
| RF04 | Enviar notificação aos destinatários quando um novo aviso for publicado |
| RF05 | O responsável confirma a leitura de um aviso |
| RF06 | Coordenação e professores acompanham quem já leu cada aviso |
| RF07 | Histórico de avisos com busca e filtros por data, turma e tipo |
| RF08 | Calendário escolar de eventos e reuniões, com confirmação de presença |
| RF09 | Secretaria cadastra alunos, turmas e responsáveis e faz o vínculo entre eles |
| RF10 | Anexar arquivos (PDF e imagens) aos avisos |

## Requisitos não funcionais

| ID | Descrição |
|----|-----------|
| RNF01 | Usabilidade: interface simples, sem treinamento, adaptada a celular |
| RNF02 | Segurança/privacidade: dados conforme a LGPD, senhas criptografadas, visibilidade restrita ao perfil |
| RNF03 | Desempenho: lista de avisos em até 3s; notificações em até 1 minuto |
| RNF04 | Disponibilidade: sistema disponível pelo menos 99% do tempo por mês |
| RNF05 | Compatibilidade: principais navegadores e Android/iOS |

## Usuários e funcionalidades

- **Responsável** — receber avisos, confirmar leitura, consultar histórico, ver calendário e confirmar presença em reuniões.
- **Professor** — publicar aviso para turma ou aluno, anexar arquivos, ver quem já leu.
- **Coordenação/Direção** — publicar avisos gerais, acompanhar leitura, gerenciar eventos.
- **Secretaria** — cadastrar alunos, turmas e responsáveis; vincular responsável ao aluno.
- **Aluno** — consultar avisos e calendário da turma.

## Histórias de usuário

**US01 — Receber avisos**
Como responsável, quero receber uma notificação quando houver um novo aviso, para não perder informações importantes.
*Critérios de aceitação:* notificação enviada em até 1 minuto após a publicação; aviso aparece na lista do responsável; funciona mesmo com o app fechado.

**US02 — Confirmar leitura**
Como responsável, quero confirmar que li um aviso, para que a escola saiba que a informação chegou até mim.
*Critérios de aceitação:* botão de "confirmar leitura" visível; hora da confirmação é registrada; aviso muda de status após confirmado.

**US03 — Publicar aviso direcionado**
Como professor, quero publicar um aviso só para minha turma, para não incomodar quem não precisa da informação.
*Critérios de aceitação:* permite escolher turma ou aluno; aviso não aparece para outras turmas; confirmação antes de publicar.

**US04 — Acompanhar confirmações de leitura**
Como professor, quero ver quem já confirmou a leitura de um aviso, para saber quem devo lembrar pessoalmente.
*Critérios de aceitação:* lista de responsáveis com status lido/não lido; atualização em tempo real; filtro por não lidos.

**US05 — Cadastrar aluno e responsável**
Como secretaria, quero cadastrar alunos, turmas e responsáveis e vinculá-los, para que os avisos cheguem à pessoa certa.
*Critérios de aceitação:* cadastro com nome, turma e responsável(is); um aluno pode ter mais de um responsável; erro exibido se faltar campo obrigatório.

**US06 — Consultar histórico de avisos**
Como responsável, quero consultar avisos antigos, para relembrar uma informação que recebi antes.
*Critérios de aceitação:* lista ordenada por data; busca por palavra-chave; filtro por turma ou tipo de aviso.

**US07 — Confirmar presença em reunião**
Como responsável, quero confirmar presença em uma reunião marcada no calendário, para que a escola saiba quantas pessoas esperar.
*Critérios de aceitação:* evento mostra data, hora e local; botão de confirmar/recusar presença; coordenação vê a lista de confirmados.

## Priorização

- **Alta:** RF01, RF02, RF03, RF04, RF05, RF06, RF09, RNF01, RNF02 — US01, US02, US03, US04, US05
- **Média:** RF07, RF10, RNF03, RNF05 — US06
- **Baixa:** RF08, RNF04 — US07

## MVP

O MVP cobre cadastro de usuários, publicação e recebimento de avisos direcionados, confirmação de leitura e acompanhamento pela escola (itens de prioridade Alta). Histórico completo, anexos e calendário de reuniões ficam para versões seguintes.

## Backlog (GitHub Project)

Colunas: **Backlog → A Fazer → Em Andamento → Em Revisão → Concluído**

Cada história de usuário e funcionalidade principal vira uma Issue com título, descrição, história de usuário, critérios de aceitação, prioridade e labels.

## Primeira Sprint

**Objetivo:** entregar o núcleo do MVP — cadastro de usuários e publicação/recebimento de avisos direcionados com confirmação de leitura.

**Funcionalidades selecionadas:** RF01 (autenticação e perfis), RF09 (cadastro de alunos/turmas/responsáveis), RF02 e RF03 (publicar e direcionar avisos), RF05 (confirmar leitura).

**Issues da Sprint:**
- US05 — Cadastrar aluno e responsável
- Implementar autenticação e perfis de acesso (RF01)
- US03 — Publicar aviso direcionado
- US02 — Confirmar leitura

**Resultado esperado:** um responsável e um professor conseguem entrar no sistema, o professor publica um aviso para a turma, e o responsável recebe e confirma a leitura — o fluxo essencial do MVP funcionando de ponta a ponta.
