# 🚗 EstudandoDjango

Projeto de aprendizado com Django, focado em explorar o funcionamento das camadas do framework, incluindo integração com banco de dados PostgreSQL, uso de Class-Based Views (CBVs), signals, autenticação e deploy em ambiente de produção (AWS EC2).

## 📚 Sobre o Projeto

Este projeto foi desenvolvido com o objetivo de aprofundar o entendimento do Django, utilizando uma estrutura de projeto realista e boas práticas de desenvolvimento web. A aplicação principal é voltada para o cadastro e gerenciamento de carros, com CRUD completo.

---

## ⚙️ Tecnologias Utilizadas

- Python 3.11+
- Django 4.2
- PostgreSQL
- HTML + Django Templates
- UWSGI + Nginx (para deploy)
- AWS EC2 (Ubuntu)
- Biblioteca `python-decouple` (para ocultar variáveis de ambiente)


---

## 📁 Estrutura de Pastas

```
estudandoDjango/
├── app/                 # Configurações globais do projeto
│   ├── settings.py
│   ├── urls.py
│   └── ...
├── cars/                # App principal (cadastro e listagem de carros)
│   ├── models.py
│   ├── views.py
│   ├── signals.py
│   └── ...
├── accounts/            # App de autenticação
│   └── ...        
├── templates/           # Templates HTML
│   └── ...
└── manage.py
```

---

## 🚀 Como Executar Localmente

1. Clone o projeto:
```bash
git clone https://github.com/matheusr-rib/estudandoDjango.git
cd estudandoDjango
```

2. Crie e ative um ambiente virtual:
```bash
python -m venv venv
source venv/bin/activate
```

3. Instale as dependências:
```bash
pip install -r requirements.txt
```

4. Configure o arquivo `.env` com suas credenciais:
```
SECRET_KEY=...
DB_NAME=carros
DB_USER=postgres
DB_PASSWORD=1436
DB_HOST=localhost
```

5. Execute as migrações e o servidor:
```bash
python manage.py migrate
python manage.py runserver
```

---

## 🌐 Deploy

O projeto está hospedado em uma instância **AWS EC2** com:

- Sistema operacional Ubuntu
- uWSGI como servidor WSGI
- Nginx como proxy reverso
- Banco de dados PostgreSQL na própria instância

---


## ☁️ Detalhes da Infraestrutura (AWS)

Este projeto foi implantado em uma instância **AWS EC2**, com as seguintes configurações:

- 🛠️ Instância: `t2.micro` (gratuita, para testes e estudos)
- 🐧 Sistema Operacional: Ubuntu 24.04 LTS.
- 🌐 IP público: [54.146.109.70/cars](http://54.146.109.70/cars) _(acesso depende do servidor estar online)_
- 🔧 Deploy com: `uWSGI` + `Nginx`, gerenciado por `systemd`
- 🗃️ Banco de Dados: PostgreSQL rodando na mesma instância EC2
- 🔐 Acesso via: chave SSH
- 🚪 Portas liberadas: 80 (HTTP)

### ⚠️ Observação
A aplicação pode não estar online permanentemente, pois este projeto tem finalidade educacional e de portfólio.

### 🔐 Variáveis de Ambiente
A aplicação utiliza a biblioteca `python-decouple` para configurar variáveis sensíveis via `.env`, tanto em desenvolvimento quanto em produção.


## ✅ Funcionalidades

- Cadastro, edição e exclusão de carros
- Upload de imagens e arquivos
- Autenticação e registro de usuários
- Geração automática de biografias de carros usando a 
- Interface amigável com templates HTML
- Deploy em produção (AWS)

---

## 🧠 Aprendizados

- Organização de apps Django com boas práticas
- Uso de Class-Based Views (CBVs)
- Criação de signals personalizados
- Deploy completo com Gunicorn, Nginx e EC2
- Configuração de arquivos estáticos e mídia

---

## 📌 Próximos Passos

- Adicionar testes automatizados
- Melhorar a segurança e autenticação
- Criar painel administrativo personalizado
- Gerar documentação da API com Swagger

---

## ✍️ Autor

Matheus Reis Ribeiro | Desenvolvedor em formação 🚀  
[LinkedIn](https://www.linkedin.com/in/matheus-ribeiro-developer/) | [GitHub](https://github.com/matheusr-rib)

---