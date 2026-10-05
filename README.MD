# Phyton IA
🤖 Chatbot com IA

Projeto desenvolvido durante meus estudos na Hashtag Treinamentos, como parte de um curso de Python e Inteligência Artificial.

A aplicação consiste em um chatbot desenvolvido com Python e Streamlit, permitindo que o usuário envie mensagens e receba respostas de um modelo de Inteligência Artificial.

🚀 Tecnologias utilizadas

🐍 Python

🎈 Streamlit

🤖 Google Gemini

🔌 OpenAI API (interface compatível com o Gemini)

📌 Funcionalidades

Interface de chat desenvolvida com Streamlit

Envio de mensagens pelo usuário

Respostas geradas por Inteligência Artificial

Histórico das mensagens durante a execução da aplicação

Utilização de st.session_state para manter o histórico da conversa

📂 Estrutura do projeto
📦 chatbot-ia
 ├── codigo.py
 └── README.md

⚙️ Como executar o projeto
1. Clone o repositório
git clone URL_DO_SEU_REPOSITORIO


Depois, entre na pasta do projeto:

cd nome-do-projeto

2. Instale as dependências

Recomendo criar um ambiente virtual antes de instalar as bibliotecas.

pip install streamlit openai

3. Configure sua chave da API

No código, configure sua chave da API:

modelo_ia = OpenAI(
    api_key="SUA_CHAVE_AQUI",
    base_url="https://generativelanguage.googleapis.com/v1beta/openai"
)


⚠️ Importante: não publique sua chave de API no GitHub. O ideal é utilizar uma variável de ambiente ou um arquivo .env que não seja enviado para o repositório.

4. Execute a aplicação

No terminal, execute:

python -m streamlit run codigo.py


O Streamlit abrirá a aplicação no navegador.

💬 Como funciona

O usuário digita uma mensagem através do componente st.chat_input().

A mensagem é armazenada no st.session_state para manter o histórico da conversa. Em seguida, o histórico é enviado para o modelo de IA:

resposta_modelo = modelo_ia.chat.completions.create(
    messages=st.session_state["lista_mensagens"],
    model="gemini-flash-lite-latest"
)


A resposta recebida é então exibida na interface e também adicionada ao histórico da conversa.

🎓 Sobre o projeto

Este projeto foi desenvolvido como projeto de estudo durante minha formação na Hashtag Treinamentos, com o objetivo de praticar conceitos de:

Python

APIs

Inteligência Artificial

Streamlit

Manipulação de estado

Desenvolvimento de aplicações interativas

📚 Próximos passos

Algumas melhorias que podem ser implementadas futuramente:

 Adicionar .env para proteger a chave da API

 Criar uma interface mais personalizada

 Adicionar botão para limpar o histórico da conversa

 Permitir selecionar diferentes modelos de IA

 Melhorar o tratamento de erros da API

 Publicar a aplicação online

⭐ Projeto desenvolvido para fins educacionais durante os estudos na Hashtag Treinamentos.
