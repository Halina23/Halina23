# Oi, eu sou a Halina 👋

Sou profissional **júnior em Dados e DevOps**, de Uberlândia-MG.

Comecei pela área de dados, com SQL, Python e Power BI. Atuei como **Analista de Dados** na **E7 Pesquisas**, um instituto de pesquisa de mercado, e hoje atuo remotamente como **DevOps Trainee** na **SoftHubCO**, há 6 meses, onde aprendo DevOps na prática. Meu objetivo é juntar as duas áreas: entender os dados e também saber colocar as aplicações no ar.

Aqui eu mostro o que já fiz em projetos reais e nos meus projetos de estudo, sempre olhando também para a parte de infraestrutura.

---

## 💼 O que já fiz em trabalhos reais

### 🏫 Análise de mercado para uma escola de educação infantil
*Analista de Dados · E7 Pesquisas (experiência anterior)*

Uma escola queria entender por que as matrículas estavam caindo e por que famílias visitavam e não se matriculavam.
- Organizei e analisei dados de **cliente oculto** de cerca de 10 escolas concorrentes: atendimento, estrutura, proposta pedagógica e preços
- Montei um **benchmark** da comunicação digital (sites e Instagram) da escola e dos concorrentes
- Separei a análise em dois eixos para o cliente: o que é **tangível** (estrutura, método) e o que é **afetivo** (atendimento, comunicação)
- Usei também dados públicos do INEP

🔧 **Olhar de DevOps:** esse projeto foi feito com planilhas e relatórios manuais. O que eu faria a seguir é levar os dados para um banco e automatizar a atualização, como fiz no meu projeto de e-commerce.

### 🌐 Site institucional da SoftHubCO
*DevOps Trainee · SoftHubCO*

- Desenvolvi o novo site da empresa em **Next.js** ([softhubco.com.br](https://softhubco.com.br))
- **Resolvi a performance no celular:** a nota no Lighthouse/PageSpeed estava em **74**. Descobri que o vídeo do topo pesava no carregamento e passei a mostrar uma imagem estática no celular, mantendo o vídeo no computador. A nota subiu para **94**.
- O site também tem nota **100** em Acessibilidade, Boas Práticas e SEO

🔧 **Parte de infra:** o site é publicado automaticamente na Hostinger pelo **GitHub Actions** a cada mudança na branch. Esse deploy foi configurado pelo meu líder e acompanhei o processo para aprender a fazer sozinha. Também coloquei landing pages em **Docker com Nginx** e corrigi problemas de configuração (Dockerfile, volumes e Compose).

### 💬 Automação de mensagens do Instagram
*DevOps Trainee · SoftHubCO*

Uma POC que recebe as mensagens diretas do Instagram da empresa, gera uma resposta com IA e prepara o lead para o CRM.
- Fluxo no **n8n**, recebendo as mensagens por **webhook** da Meta
- Resposta automática gerada com **Gemini** e enviada pela API do Instagram

🔧 **Parte de infra:** subi o n8n **self-hosted em Docker**, expus o serviço com **túnel HTTPS (ngrok)** para a Meta conseguir chamar o webhook e configurei a **validação de assinatura HMAC SHA-256**, que garante que a mensagem veio mesmo da Meta. Os tokens e segredos ficam em credenciais, fora do código.

### 🔍 SEO técnico no site de um cliente
*DevOps Trainee · SoftHubCO*

Site antigo em PHP (CodeIgniter) com problemas de indexação no Google.
- Converti **902 imagens para WebP**, deixando as páginas mais leves
- Criei redirecionamentos **301** para cerca de **380 links quebrados**
- Corrigi URLs canônicas e limpei os sitemaps no **Google Search Console**
- Automatizei a coleta de evidências de SEO com **Python + Selenium** e gerei um relatório de auditoria em PDF

🔧 **Parte de infra:** montei o **ambiente local em Docker** (PHP 8.1 + Apache + MySQL), atualizei o código para funcionar no PHP 8, tirei senhas do código para um **`.env`**, usei **curl** para checar respostas do servidor e identifiquei que alguns problemas precisavam ser resolvidos no **Nginx** de produção. Todo o trabalho foi feito em **branches e Pull Requests** revisados.

---

## 📂 Projetos de estudo

### 🔗 [encurtador-links](https://github.com/Halina23/encurtador-links)
Um encurtador de links (tipo Bit.ly) que criei para **aprender o caminho de uma aplicação até a produção**.
- API em Python (FastAPI) com banco PostgreSQL
- Rodando em Docker, com testes automáticos e verificação de segurança no GitHub Actions
- Logs e métricas para acompanhar a aplicação
- 🚧 **Próximo passo:** fazer o deploy em uma VPS com Ansible e k3s

### ⚙️ [gitops-pipeline-com-gate-de-qualidade](https://github.com/Halina23/gitops-pipeline-com-gate-de-qualidade)
Meu **primeiro projeto completo de DevOps**: um ambiente Kubernetes montado do zero no meu computador.
- Criei a máquina virtual com OpenTofu e configurei com Ansible
- Instalei um cluster k3s e usei Argo CD para fazer deploy a partir do Git
- Fiz um "porteiro" com IA (Gemini) que revisa o código antes do deploy
- Documentei os problemas que enfrentei e como resolvi cada um

### 🛒 [ecommerce-data-pipeline-postgresql](https://github.com/Halina23/ecommerce-data-pipeline-postgresql)
Projeto de dados de um e-commerce com loja física, **do banco de dados até a análise**.
- Modelei o banco no PostgreSQL, com regras de estoque e vendas
- Extraí e tratei os dados com Python (Pandas)
- Fiz análises e dashboards no Power BI
- Encontrei e documentei um erro nos dados, mantendo o original para auditoria

### 🤖 [Agente-Text-To-SQL](https://github.com/Halina23/Agente-Text-To-SQL)
Um assistente com IA que transforma perguntas em português em consultas SQL.
- Python + Gemini + PostgreSQL

---

## 🛠️ Ferramentas que já usei

**Dados:** SQL · PostgreSQL · MySQL · Python · Pandas · Power BI · Excel

**DevOps:** Linux · Git · Docker · Nginx · GitHub Actions · k3s · Argo CD · Ansible · OpenTofu

**APIs e automação:** FastAPI · n8n · Webhooks · Gemini API · Selenium

**Web e SEO:** Next.js · PHP · Google Search Console · Lighthouse

---

## 📚 O que estou aprendendo agora

- Fazer deploy de verdade (VPS + k3s) com o encurtador-links
- Monitoramento com Grafana e Prometheus
- AWS, estudando para a certificação

---

## 📫 Contato

- LinkedIn: [linkedin.com/in/halina-oliveira](https://linkedin.com/in/halina-oliveira)
- E-mail: halina.oliveira2021@gmail.com
