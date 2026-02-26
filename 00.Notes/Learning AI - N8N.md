# Ai Agents x Automations 

## Ai Agents

**Definition:**  
AI agents are autonomous, decision-making entities that **perceive**, **reason**, and **act** in a dynamic environment — often using tools like LLMs (e.g., GPT), memory, and a chain of reasoning.

**Key Features:**

- **Goal-oriented**: You give them a goal, and they figure out the steps.
- **Context-aware**: They remember past steps and adapt behavior accordingly.
- **Autonomous decision-making**: Choose what action to take based on current data/state.
- **Can handle unexpected input**: Flexible and can adjust mid-task.

**Example:**  
"Research top AI tools, summarize them, and email the best 3 to me."  
An AI agent will:

- Search the web
    
- Read and filter results
    
- Rank them
    
- Write a human-like summary
    
- Compose and send an email

---
## Automations 

**Definition:**  
Automations are predefined sequences of tasks or workflows — **IF X happens, do Y**. 

They’re rule-based and deterministic.

**Key Features:**

- **Scripted flows**: No dynamic decision-making.
- **Trigger-response**: Executes based on events (e.g., new row in Airtable triggers a Slack message).
- **Limited context**: Doesn’t "think" beyond the logic you define.
- **Reliable and fast**: Great for repetitive tasks.

**Example:**  
"When a user signs up, send them a welcome email."  
This is a basic automation — no intelligence, no variation.

----

# How Servers & Docker Work 

Servers are computers designed to provide services or data to other computers over a network. For example, when you visit a website, your browser makes a request to a web server, which responds with HTML, CSS, images, etc.

**Docker** is a tool that allows you to package an application and all its dependencies into a **container**. Think of a container as a lightweight, portable mini-computer that runs only what's needed for your app — isolated from your main system.

#### Why Use Docker?

- Consistency across development and production
- Isolation between apps
- Easy to start/stop/test environments

When you run a Docker container, it's like spinning up a small virtual machine (VM) that runs your app. But unlike traditional VMs, Docker containers share the host OS kernel, making them much more lightweight.

# N8N How This Work

## **Who is this tool for?**

- No-Code / Low-Code Beginners
- Fast Prototypers
- Developers who want to automate tasks quickly
- Technical founders / Indie hackers
- Business analysts and operations teams

- **Yes, if you want:**
    - Rapid automation without writing much code
    - Workflow Templates to speed up dev
    - Easy AI integrations (like ChatGPT, Claude, etc.)
    - API connections with hundreds of services
    - Scheduled or event-triggered automation
    - Self-hostable automation platform
- **Not Ideal, if you:**
    - Prefer full control through code
    - Need advanced, low-latency logic
    - Are working on highly customized backend systems

---

## Core Nodes 

Esses são os nodes que você precisa aprender e dominar para conseguir criar qualquer automação. 

- Code
	- Executar **JavaScript ou Python** para manipular dados.
	- **Run once for all items** → Executa 1 vez pegando todos os itens.
	- **Run once for each item** → Executa uma vez para cada item (loop automático).
- Edit Fields
	- Organizar e estruturar os dados.
		- Renomear campos
		- Criar novos campos
		- Preparar dados para enviar pro google Sheets
		- *Use quando você quer "arrumar" os dados antes de enviar para outro sistema.*
- Filter
	- Filtrar dados com base em condições.
		- Exemplo:
		- Mostrar apenas capítulos > 4
		- Filtrar leads quentes
		- Filtrar valores maiores que X
	- Use quando você quer manter apenas dados que atendem uma condição.
- If
	- Criar dois caminhos: Verdadeixo x Falso
	- Exemplo: Se capítulo > 8 → caminho A 
	- Senão → caminho B
- Switch
- Merge
- Loop Over Items
- Convert to File
- Extract from File
- HTTP Request
- Execute Command
- Webhook + Respond to Webhook

