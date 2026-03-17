https://github.com/user-attachments/assets/9b0ec02c-5f16-4093-a031-2f9b1acf9414
# 🚀 Arquitetura de Automação & RevOps (Event-Driven)

Bem-vindo ao repositório de demonstração da arquitetura de **Revenue Operations (RevOps)** que desenvolvi para unificar as frentes de Atendimento, Marketing e Vendas.

O objetivo deste ecossistema é simples: **eliminar o "copiar e colar" da operação, acabar com os silos de dados corporativos e escalar o faturamento através da tecnologia.**

## 🛠️ Stack Tecnológica & Infraestrutura

Toda a solução foi projetada sob uma arquitetura de microsserviços e provisionada em nuvem.

* **Infraestrutura:** Linux (VPS), Docker, Docker Swarm, Portainer.
* **Orquestração & Lógica:** n8n, Webhooks, APIs REST, JavaScript, RegEx.
* **Inteligência Artificial:** Google Gemini (LLM via API).
* **Bancos de Dados & Fila:** PostgreSQL, Redis, RabbitMQ.
* **Plataformas de Negócio:** Chatwoot (Omnichannel), Mautic (Automação de Marketing), PipeRun (CRM).

## ⚙️ Como o Motor Funciona (O Fluxo de Dados)

Esta é uma arquitetura orientada a eventos (*Event-Driven*). Nenhum processo depende de ação manual do usuário.

1. **Captura do Evento:** O cliente interage com a equipe de atendimento via WhatsApp/Web através do **Chatwoot**.
2. **Gatilho Assíncrono:** Um Webhook dispara o evento silenciosamente para o motor de orquestração (**n8n**).
3. **Leitura e Tratamento (Shadow Logging):** O n8n recebe o JSON, faz a validação dos dados em voo (utilizando RegEx e JavaScript) e garante que o histórico da conversa seja salvo.
4. **Injeção de Inteligência (IA):** A API do **Google Gemini** analisa o contexto da conversa em tempo real e elabora um *Pitch de Vendas* (diagnóstico comercial sob medida) com base nas dores relatadas pelo lead.
5. **Distribuição para o CRM:** O n8n consome a API REST do **PipeRun** e injeta todas as informações organizadas diretamente no funil do vendedor, incluindo o Pitch gerado pela IA. Em paralelo, o lead é tagueado no **Mautic** para réguas de nutrição.

## 📊 Impacto no Negócio

* **SLA de Atendimento:** Redução a zero do tempo de triagem manual e preenchimento de CRM.
* **Governança:** Integridade absoluta dos dados (nenhum contato se perde entre o Atendimento e Vendas).
* **Conversão:** Vendedores abordam os leads com contexto total e um discurso (Pitch) já otimizado pela Inteligência Artificial.

---
*Desenvolvido por **Jheyson Silva Siqueira*** *Engenheiro de Automação & RevOps | Integração de Sistemas* 🔗 [Conecte-se comigo no LinkedIn](https://www.linkedin.com/in/jheyson-silva-siqueira)
