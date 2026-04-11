## 📌 Visão Geral

Este projeto tem como objetivo criar um bot em Python capaz de simular múltiplos usuários reais acessando um funil (quiz + formulário de email), utilizando técnicas avançadas de automação para evitar detecção.

O bot executa sessões independentes que replicam o comportamento humano, incluindo navegação, interação com quiz e preenchimento de formulário.

---
## 🎯 Objetivos

- Simular acessos reais ao funil
- Navegar automaticamente por um quiz interativo
- Preencher emails reais a partir de uma lista (.txt)
- Alternar entre usuários que convertem e usuários que abandonam
- Utilizar proxies rotativos para cada sessão
- Utilizar user-agents mobile personalizados (Os que eu irei passar)

---

## ⚙️ Funcionalidades Principais

### 🔁 Gerenciamento de Sessões

- Criação de múltiplas sessões simultâneas ou sequenciais
- Cada sessão representa um usuário único
- Controle de comportamento por sessão (converter ou não)

### 🌐 Navegação Automatizada

- Acesso ao link principal
- Execução do fluxo completo do quiz
- Interação com botões e opções
- Simulação de delays humanos

### 📧 Manipulação de Emails

- Leitura de arquivo `emails.txt`
- Uso único por sessão
- Preenchimento apenas em sessões selecionadas

### 🎭 Simulação de Comportamento Humano

- Delays aleatórios entre ações
- Abandono aleatório do funil
- Tempo variável de permanência

### 📱 User-Agent Mobile

- Uso de user-agents reais de dispositivos móveis
- Rotação entre diferentes perfis (Android/iOS)
    

### 🌍 Sistema de Proxies

- Um proxy por sessão
- Suporte a proxies HTTP/SOCKS
- Rotação automática

### 🎲 Randomização Inteligente

- Controle de probabilidades:
    
    - Usuários que convertem
    - Usuários que abandonam
    - Usuários que apenas navegam

---

## 🛠️ Tecnologias Utilizadas

- Python 
- Playwright (automação de navegador)
- Asyncio (execução assíncrona)
- Random / Time (simulação de comportamento)

---

## 🔄 Fluxo de Execução

1. Carregar listas (emails, proxies, user-agents)
    
2. Iniciar sessão
    
3. Definir comportamento da sessão
    
4. Aplicar proxy e user-agent
    
5. Acessar página
    
6. Executar quiz
    
7. Decidir:
    - Preencher email
    - Abandonar
8. Encerrar sessão
9. Repetir processo

---

## 🚨 Boas Práticas

- Utilizar proxies de qualidade (residenciais ou mobile)
    
- Evitar padrões fixos de comportamento
    
- Inserir delays realistas
    
- Monitorar erros e exceções
    
- Limitar volume de requisições por minuto
    

---
## ⚠️ Aviso

Esse site é meu, é uma automação somente para fins internos da nossa empresa. 

---
## 💡 Possíveis Melhorias Futuras
- Dashboard de monitoramento
- Logs detalhados por sessão
- Integração com banco de dados
- Distribuição em múltiplos servidores
- Uso de fingerprints avançados

---
