https://github.com/user-attachments/assets/27d99e9d-e7c8-481b-9e11-a5f00927b4a6

#  Enterprise Automation Engine & RevOps (Event-Driven)

![n8n](https://img.shields.io/badge/n8n-FF6D5A?style=for-the-badge&logo=n8n&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)
![Google Gemini](https://img.shields.io/badge/Google_Gemini-8E75B2?style=for-the-badge&logo=googlebard&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![APIs REST](https://img.shields.io/badge/API_REST-005571?style=for-the-badge&logo=json&logoColor=white)

Bem-vindo ao repositório de demonstração da arquitetura de integração de alto impacto que desenvolvi para unificar as frentes de Atendimento, Marketing e Vendas.

O objetivo deste ecossistema é simples: **eliminar o "copiar e colar" da operação, acabar com os silos de dados corporativos e escalar o faturamento através da tecnologia e Inteligência Artificial.**

## Stack Tecnológica & Infraestrutura

Toda a solução foi projetada sob uma arquitetura de microsserviços e provisionada em nuvem.

* **Infraestrutura:** Linux (VPS Hetzner), Docker, Docker Swarm, Portainer.
* **Orquestração & Lógica:** n8n, Webhooks, APIs REST, Node.js, RegEx.
* **Inteligência Artificial:** Google Gemini Pro (LLM via API).
* **Bancos de Dados & Mensageria:** PostgreSQL, Redis, RabbitMQ.
* **Plataformas de Negócio:** Chatwoot (Omnichannel), Mautic (Automação de Marketing), PipeRun (CRM).

## Como o Motor Funciona (O Fluxo de Dados)

Esta é uma arquitetura orientada a eventos (*Event-Driven*). Nenhum processo depende de ação manual do usuário.

1. **Captura do Evento:** O cliente interage com a equipe de atendimento via WhatsApp/Web através do **Chatwoot**.
2. **Gatilho Assíncrono:** Um Webhook dispara o evento silenciosamente para o motor de orquestração (**n8n**).
3. **Leitura e Tratamento (Shadow Logging):** O n8n recebe o payload JSON, faz a validação dos dados em voo (utilizando RegEx e JavaScript) e garante que o histórico da conversa seja salvo.
4. **Injeção de Inteligência (IA):** A API do **Google Gemini Pro** analisa o contexto da conversa em tempo real e elabora um *Pitch de Vendas* (diagnóstico comercial sob medida) com base nas dores relatadas pelo lead.
5. **Distribuição para o CRM:** O n8n consome a API REST do **PipeRun** e injeta todas as informações estruturadas diretamente no funil de vendas, incluindo o diagnóstico da IA. Em paralelo, o lead é tagueado no **Mautic** para réguas de nutrição.

## Impacto no Negócio

* **Zero Data Entry:** Eliminação de 100% da digitação e triagem manual de leads para o CRM.
* **SLA de Atendimento:** O tempo decorrido entre a captação e o roteamento caiu para milissegundos.
* **Governança:** Integridade absoluta dos dados (nenhum contato se perde entre o Atendimento e Vendas).
* **Conversão Assistida por IA:** Vendedores abordam os leads com contexto total e um discurso (*Pitch*) já otimizado pela Inteligência Artificial.

---
*Desenvolvido por **Jheyson Silva Siqueira*** *Engenheiro de Automação & Integrações | AI Builder* 🔗 [Conecte-se comigo no LinkedIn](https://www.linkedin.com/in/jheyson-silva-siqueira)
