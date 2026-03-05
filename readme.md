# EduTok — Plataforma Educacional Inteligente

> **Documento de Apresentação para a Secretaria de Educação**
> Versão 1.3 · Março de 2026

---

## 1. Visão Geral

O **EduTok** é uma plataforma educacional completa, projetada para transformar a comunicação e o acompanhamento pedagógico nas escolas públicas. Integra alunos, professores, responsáveis e gestores em um único ecossistema digital, com inteligência artificial embarcada para personalizar o aprendizado e facilitar a gestão escolar.

### Objetivos Principais

- **Conectar** todos os agentes da comunidade escolar em um ambiente seguro e moderno
- **Automatizar** processos acadêmicos como lançamento de notas, criação de eventos e geração de exercícios
- **Personalizar** o ensino com IA adaptativa que identifica lacunas de aprendizagem
- **Fornecer transparência** aos responsáveis sobre o desempenho e a rotina escolar dos filhos
- **Empoderar gestores** com painéis de dados e ferramentas administrativas completas

---

## 2. Arquitetura da Plataforma

| Componente         | Tecnologia                                |
| ------------------- | ----------------------------------------- |
| Frontend            | React + TypeScript, Vite, Tailwind CSS    |
| Backend             | Node.js + Express                         |
| IA Assistente       | Eduna 1.3 Pro (modelo proprietário)       |
| Comunicação em tempo real | WebSockets                          |
| Banco de Dados      | PostgreSQL com armazenamento local VPS     |
| Hospedagem          | VPS dedicado                              |

O aplicativo é uma **Progressive Web App (PWA)**, o que significa que funciona em qualquer navegador moderno, pode ser instalado na tela inicial do celular e oferece experiência nativa sem precisar da Play Store ou App Store.

---

## 3. Painéis e Funcionalidades por Perfil

### 3.1 📚 Painel do Aluno

O aluno acessa um ambiente moderno e intuitivo com as seguintes funcionalidades:

#### Dashboard Inteligente
- **Próxima Aula** — Widget em tempo real que mostra a próxima aula do dia, com matéria, horário e sala
- **Acesso Rápido** — Atalhos diretos para as funcionalidades mais usadas (Notas, Chat, Calendário, IA)
- **Desempenho Acadêmico** — Visão geral das notas por matéria com gráficos de evolução
- **Próximos Eventos** — Lista dos eventos e datas importantes da escola
- **Sequência de Estudos** — Gamificação que acompanha dias consecutivos de estudo

#### Eduna 1.3 Pro — Assistente de IA
- **Chat com IA** personalizado para cada aluno, com saudações e comportamento adaptados ao perfil
- **Transcrição de voz** — O aluno pode enviar mensagens de voz e a IA transcreve automaticamente
- **Contexto escolar** — A IA tem acesso ao histórico de notas e atividades do aluno para fornecer respostas personalizadas
- **Suporte multilínguas** — Responde em português adequado à linguagem estudantil

#### EduGen — Gerador de Exercícios com IA
- **Exercícios personalizados** por matéria, série e tópico
- **Correção automática** com explicações detalhadas
- **Acompanhamento de erros** — Sistema de "caderno de erros" que identifica padrões de dificuldade
- **Progressão adaptativa** — Exercícios ajustados ao nível do aluno
- **Exportação em PDF** dos exercícios e resultados
- **Compartilhamento na eFeed** — O aluno pode publicar seus resultados na rede social da escola
- Disciplinas disponíveis: Matemática, Português, História, Geografia, Ciências, Inglês, Artes, Educação Física

#### Boletim Digital
- **Visualização completa das notas** por matéria e bimestre
- **Cálculo automático de média** com indicação visual (verde, amarelo, vermelho)
- **Exportação do boletim em PDF** formatado profissionalmente
- **Histórico de evolução** por período

#### Calendário Escolar
- **Visualização mensal** com destaque para eventos e provas
- **Modo Aulas** — Visualização do horário de aulas do aluno por dia
- **Modo Eventos** — Lista de eventos escolares com detalhes
- **Navegação por data** com seleção rápida

#### eFeed — Rede Social Escolar
- **Feed de publicações** — Posts com texto, fotos e enquetes
- **Stories** — Publicações temporárias com fotos
- **Reações e comentários** no estilo das redes sociais mais populares
- **Seguir/deixar de seguir** outros usuários
- **Bookmarks** para salvar publicações favoritas
- **Verificação de perfil** para professores e gestores

#### Chat em Tempo Real
- **Grupo da Turma** — Chat coletivo com todos os colegas da turma
- **Conversa privada com Professores** — O aluno pode iniciar conversas diretas com seus professores (necessita aprovação do professor)
- **Mensagens de voz** — Gravação e envio de áudio com visualização de ondas sonoras
- **Envio de mídia** — Fotos, vídeos e documentos
- **Reações com emojis** em mensagens
- **Responder e citar** mensagens anteriores (swipe-to-reply)
- **Transcrição de áudio** com IA
- **Resumo de vídeos** com IA
- **Menções (@)** para notificar colegas

#### Perfil do Aluno
- **Foto de perfil** personalizável
- **Dados acadêmicos** (turma, escola, série)
- **Sequência de estudos** e estatísticas de uso
- **Atividades recentes** com histórico

#### Biblioteca de Recursos
- **Materiais didáticos** organizados por matéria
- **Download de apostilas, resumos e materiais complementares**
- **Categorização** por tipo (PDF, vídeo, link, imagem)
- **Busca inteligente** por palavra-chave

---

### 3.2 👨‍🏫 Painel do Professor

O professor possui ferramentas específicas para gestão pedagógica:

#### Dashboard do Professor
- **Próxima Aula** — Horário da próxima aula do dia
- **Acesso Rápido** — Atalhos para Notas, Eventos, Chat e Escola Panel
- **Eventos pendentes** — Resumo dos próximos compromissos

#### Lançamento de Notas (`ProfessorNotas`)
- **Seleção de turma** — Escolha entre as turmas atribuídas ao professor
- **Listagem de alunos** por turma com avatares e identificação visual
- **Lançamento por matéria** — Seleção da disciplina (Matemática, Português, História, etc.) e bimestre
- **Interface intuitiva** — Campo de nota para cada aluno com validação
- **Salvamento no servidor** — Notas armazenadas de forma segura com sincronização
- **Indicação de status** — Cores automáticas: verde (≥7), amarelo (≥5), vermelho (<5)

#### Criação e Gestão de Eventos (`ProfessorEventos`)
- **Criação de eventos escolares** — Provas, reuniões, atividades culturais, feriados, entregas, etc.
- **Seleção por turma(s)** — O evento pode ser direcionado a turmas específicas
- **Tipos de evento** com ícones e cores distintas (prova, reunião, excursão, entrega, feriado, outro)
- **Edição e exclusão** de eventos existentes
- **Integração com o calendário** — Os eventos criados aparecem automaticamente no calendário de alunos e responsáveis

#### Chat do Professor
- **Grupo da Turma** — Participação no chat da turma para comunicações gerais
- **Grupo dos Professores** — Chat exclusivo entre professores da mesma escola
- **Conversas com Alunos** — Atendimento individual com aprovação/rejeição de solicitações
- **Filtros avançados** — Todos, Alunos, Pendentes
- **Busca de alunos** — Pesquisa por nome no banco de dados da escola para iniciar conversa
- **Turmas Arquivadas** — Acesso ao histórico de conversas de turmas anteriores

#### Eduna 1.3 Pro para Professores
- **Saudação personalizada** — "Olá, professor(a)! Sou a Eduna 1.3 Pro, sua assistente de IA da escola."
- **Apoio pedagógico** — Sugestões de atividades, estratégias de ensino e planejamento
- **Análise de desempenho** — Auxílio na interpretação de dados acadêmicos

---

### 3.3 👪 Painel do Responsável (Pai/Mãe)

O responsável tem acesso a um painel focado no acompanhamento do(s) filho(s):

#### Seleção de Filhos
- **Múltiplos filhos** — Se o responsável tem mais de um filho na rede, pode alternar entre eles com um seletor na parte superior
- **Dados por filho** — Todas as informações (notas, calendário, chat) são filtradas pelo filho selecionado

#### Dashboard do Responsável
- **Próxima Aula do Filho** — Mostra a próxima aula com matéria e horário
- **Acesso Rápido** — Notas, Calendário, Chat (com filtro por filho)
- **Desempenho do Filho** — Gráfico com as notas do filho selecionado
- **Eventos Próximos** — Compromissos escolares do filho

#### Acompanhamento de Notas
- **Boletim completo do filho** com notas por matéria e bimestre
- **Média geral** calculada automaticamente
- **Exportação em PDF** do boletim do filho

#### Calendário
- **Visualização completa** dos eventos e aulas do filho
- **Modo Aulas** — Horário semanal do filho
- **Modo Eventos** — Provas, reuniões, entregas

#### Chat do Responsável
- **Grupo da Turma** — Acompanhamento das conversas da turma do filho
- **Conversas individuais** com professores (via solicitação aprovada pelo professor)

> **Nota de segurança**: Os responsáveis **não** têm acesso à seção "Equipe da Escola" nem são contactáveis diretamente por professores pelo chat. Toda comunicação formal é mediada pelo grupo da turma.

#### Eduna 1.3 Pro para Responsáveis
- **Saudação específica** — "Olá! Sou a Eduna 1.3 Pro, a assistente IA da escola."
- **Informações pedagógicas** — Orientações sobre acompanhamento escolar e dicas de estudo

---

### 3.4 🏫 Painel da Escola (Gestão Escolar)

O painel administrativo da escola oferece ferramentas completas de gestão:

#### Gestão de Turmas
- **Criação e edição de turmas** com nome, série e professor responsável
- **Listagem de alunos** por turma com dados completos (nome, CPF, data de nascimento)
- **Editor de horários** — Definição dos horários de aula por dia da semana com matéria, hora de início e fim
- **Adicionar/remover slots de horário** dinamicamente
- **Exportação PDF** — Lista de alunos da turma com dados formatados profissionalmente

#### Gestão de Professores
- **Cadastro de professores** com dados pessoais
- **Atribuição de disciplinas e turmas**
- **Verificação de registro** — Status de verificação no sistema
- **Edição e exclusão** de registros

#### Gestão de Alunos
- **Cadastro completo** com nome, CPF, data de nascimento, turma, série
- **Transferência entre turmas** — Alterar a turma de um aluno com um clique
- **Edição de dados** — Atualização de informações pessoais
- **Vínculo com responsáveis** — Visualização dos responsáveis cadastrados

#### Gestão de Responsáveis
- **Cadastro de pais/mães** com telefone e vínculo aos filhos
- **Permitir/gerenciar múltiplos filhos** por responsável

#### Estatísticas e Relatórios
- **Contadores em tempo real** — Número de turmas, professores, alunos e responsáveis
- **Exportação de relatórios** em PDF

---

### 3.5 🏛️ Painel da Secretaria de Educação

O nível mais alto de gestão, com visão ampla de toda a rede:

#### Gestão de Escolas
- **Cadastro de escolas** — Nome, endereço completo com busca automática por CEP
- **Slug automático** — Geração de identificador único para cada escola
- **Foto da escola** — Upload de imagem representativa
- **Listagem com busca** — Pesquisa por nome entre todas as escolas da rede

#### Gestão Centralizada de Professores
- **Cadastro de professores** vinculados a uma ou mais escolas
- **Atribuição de disciplinas** (Matemática, Português, Ciências, etc.)
- **Definição de cargo** (Professor, Diretor, Coordenador)
- **Verificação automática** — Hash de CPF e data de nascimento para segurança

#### Visão da Rede
- **Panorama geral** com contadores de escolas, professores e alunos
- **Navegação por escola** — Visualização detalhada de cada unidade escolar

---

## 4. Recursos Transversais (Todos os Perfis)

| Recurso                  | Descrição                                                                 |
| ----------------------- | ------------------------------------------------------------------------- |
| **Tour Guiado**          | Tutorial interativo para novos usuários com destaque visual (spotlight)     |
| **Notificações**         | Sistema de notificações em tempo real via WebSocket                        |
| **Tema Claro/Escuro**    | Alternância automática ou manual de tema                                   |
| **Responsividade**       | Interface otimizada para celular, tablet e desktop                         |
| **PWA**                  | Instalável como app nativo sem loja de aplicativos                         |
| **Segurança**            | Sessões autenticadas, CSRF protection, hash de dados sensíveis             |
| **Acessibilidade**       | Navegação por teclado, textos alternativos, contraste adequado             |
| **Relatório de Problemas** | Shake-to-report: agite o celular para reportar um bug rapidamente        |

---

## 5. Inteligência Artificial — Eduna 1.3 Pro

A **Eduna 1.3 Pro** é a assistente de IA integrada ao EduTok, projetada especificamente para o contexto educacional brasileiro.

### Capacidades

- **Chat inteligente** — Respostas contextualizadas para alunos, professores e responsáveis
- **Geração de exercícios** — Criação automática de questões por matéria, série e tópico
- **Correção automática** — Avaliação instantânea com explicações pedagógicas
- **Transcrição de áudio** — Converte mensagens de voz em texto com precisão
- **Resumo de vídeos** — Extrai e sintetiza o conteúdo de vídeos compartilhados
- **Caderno de erros** — Registra e acompanha os erros recorrentes de cada aluno
- **Personalização por perfil** — Linguagem e funcionalidades adaptadas ao tipo de usuário

### Diferenciais Pedagógicos

- Abordagem construtivista com exercícios progressivos
- Foco no desenvolvimento da autonomia do aluno
- Feedback formativo detalhado (não apenas "certo" ou "errado")
- Integração com o currículo escolar e BNCC

---

## 6. Comunicação e Segurança

### Modelo de Comunicação

```
┌──────────────────────────────────────────────┐
│              Grupo da Turma                   │
│    Alunos + Professores + Responsáveis        │
└──────────────────────────────────────────────┘

┌──────────────────────────────────────────────┐
│         Grupo dos Professores                 │
│              Apenas Professores               │
└──────────────────────────────────────────────┘

┌──────────────────────────────────────────────┐
│          Conversas Privadas                   │
│   Aluno ↔ Professor (com aprovação)          │
│     (Responsáveis não contactam               │
│      professores diretamente)                 │
└──────────────────────────────────────────────┘
```

### Proteções Aplicadas

- **Aprovação obrigatória** — O professor deve aprovar cada solicitação de conversa privada
- **Segmentação de acesso** — Cada perfil vê apenas o que é relevante para seu papel
- **Hash de dados sensíveis** — CPFs e datas de nascimento são armazenados como hash
- **Sessões seguras** — Autenticação com cookies httpOnly e proteção CSRF
- **Purga automática de mídia** — Anexos antigos são automaticamente substituídos para economia de armazenamento

---

## 7. Infraestrutura e Escalabilidade

- **Servidor VPS dedicado** com Node.js e PostgreSQL
- **WebSocket** para comunicação em tempo real (mensagens, notificações, atualizações de dados)
- **Service Worker** para funcionamento offline parcial e cache inteligente
- **Compressão de mídia** — Imagens e vídeos são otimizados antes do envio
- **Backup automático** dos dados com sistema de persistência local

---

## 8. Benefícios para a Rede de Ensino

| Benefício                          | Impacto                                                        |
| ---------------------------------- | -------------------------------------------------------------- |
| **Centralização da comunicação**   | Redução de grupos de WhatsApp informais e dispersos            |
| **Transparência acadêmica**        | Responsáveis acompanham notas e eventos em tempo real          |
| **Exercícios personalizados**      | IA adapta conteúdo ao nível individual de cada aluno           |
| **Redução de burocracia**          | Notas, boletins e relatórios gerados automaticamente           |
| **Gestão centralizada**            | Secretaria gerencia todas as escolas em um único painel        |
| **Custo zero de distribuição**     | PWA elimina necessidade de publicação em lojas de apps         |
| **Engajamento estudantil**         | eFeed e gamificação incentivam participação ativa              |
| **Segurança da informação**        | Dados protegidos com criptografia e controle de acesso         |

---

## 9. Contato e Próximos Passos

A plataforma EduTok está pronta para implantação piloto na rede municipal de ensino. Para iniciar o processo de integração, sugerimos os seguintes próximos passos:

1. **Reunião de apresentação detalhada** com demonstração ao vivo da plataforma
2. **Seleção de escola(s) piloto** para validação em ambiente real
3. **Treinamento da equipe gestora** e professores participantes
4. **Feedback iterativo** com ajustes baseados na experiência dos usuários
5. **Expansão gradual** para toda a rede municipal

---

> *EduTok — Transformando a educação com tecnologia e inteligência artificial.*
