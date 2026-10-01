# Introduction to Flask

[English](README.md)

## Ideia e processo

Site de aula Flask sobre Thorin & Company, uma companhia fictícia. Código revisado em 01/10/2026. Não foram encontrados planejamento datado ou wireframes nos arquivos revisados. Site educacional, não empresa real, serviço de contato ou produto de produção original.

## Arquitetura e design

`run.py` cria a aplicação Flask. Rotas renderizam home, about, member, contact e careers. About/member leem `data/company.json`. Template base usa Bootstrap e tema Clean Blog com imagem hero, navegação e blocos herdados. Assets e personagens fictícios mantêm seus direitos originais.

POST de contato só mostra agradecimento com o nome informado. A rota revisada não envia email ou salva mensagem, apesar do texto da página dizer que envia.

## Execução local

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
export SECRET_KEY='replace-with-a-local-development-key'
export IP=127.0.0.1
export PORT=5000
python run.py
```

Requirements fixa Flask 1.1.2 e dependências históricas; compatibilidade não testada. SECRET_KEY vem do ambiente. `run.py` sempre liga debug: mantenha local. Procfile usa `python run.py`, não servidor endurecido de produção.

## Testes e limites

Suíte não encontrada na listagem revisada da raiz. Aplicação e testes não executados; deploy público atual não confirmado. Verifique rotas, nomes inexistentes, erros de arquivo/schema JSON, navegação mobile e validação com dados fictícios. Membro inexistente recebe objeto vazio, sem 404 explícito. Rota de contato não tem CSRF ou validação explícita dos campos no servidor. Não use mensagens pessoais reais nesse formulário de aula.

## Capturas

Nenhuma captura verificada ou adicionada. Capture home/about/contact após verificação local, em arquivos datados sob `docs/assets/`, com dados fictícios. Identifique a resposta do contato como confirmação demonstrativa, não entrega de email.

## Créditos e licença

Material de template/curso do Code Institute e dependências mantêm direitos originais, sem licença nova. README original preservado no [apêndice em inglês](README.md#original-readme), como referência histórica.
