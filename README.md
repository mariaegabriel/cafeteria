☕ Momento Café

Site de uma cafeteria fictícia, feito em HTML, CSS e JavaScript com Bootstrap 5. O projeto reúne a página inicial, o cardápio com pedido (balcão, mesas e delivery), login, cadastro, acompanhamento de pedidos, contato e uma área administrativa para o gerente.

Projeto de estudo. Não há servidor nem banco de dados: os dados ficam no navegador (localStorage).

Sumário
Páginas
Funcionalidades
Tecnologias
Estrutura de pastas
Como executar
Identidade visual
Dados salvos no navegador
Estado do projeto
Autoria
Páginas
Página	Arquivo	O que faz
Início	index.html	Apresentação da cafeteria (Home e Sobre)
Produtos	templates/produtos.html	Cardápio com 21 itens, busca, filtros e painel "Meu pedido"
Pedidos	templates/pedidos.html	Acompanhamento dos pedidos do cliente (área com login)
Login	templates/login.html	Entrada como Cliente ou Gerente
Cadastro	templates/cadastro.html	Criação de conta com validação
Contato	templates/contato.html	Formulário, horários, endereço e perguntas frequentes
Administrativo	templates/admin.html	Painel do gerente com pedidos em atendimento e finalizados
Funcionalidades

Cardápio e pedido (Produtos)

7 categorias: Bebidas Quentes, Bebidas Geladas, Padaria e Confeitaria, Lanches Salgados, Sobremesas, Opções Saudáveis e Produtos para Venda.
Busca por nome, descrição ou categoria, sem diferenciar acentos (digitar "pao" encontra "Pão de Queijo").
Filtros por categoria, combinados com a busca.
Painel lateral "Meu pedido", com quantidades, total e carrinho que continua salvo ao recarregar a página.
Três formas de atendimento: balcão, mesas (escolha do número da mesa) e delivery (endereço e telefone).

Conta de usuário

Cadastro com validação de nome, e-mail, telefone (com máscara), senha e confirmação.
Indicador de força da senha e botão para mostrar ou ocultar a senha.
Conta de Cliente ou de Gerente (a de gerente exige um código de acesso).

Contato

Formulário com validação e contador de caracteres.
Horário de funcionamento com o selo "Aberto agora" ou "Fechado agora".
Perguntas frequentes em acordeão.

Administrativo

Menu lateral com abas "Em atendimento" e "Finalizados".
Cartões de resumo (pedidos do dia, em atendimento, finalizados e faturamento).
Tecnologias
HTML5 e CSS3
JavaScript (puro, sem bibliotecas)
Bootstrap 5.3.8
Bootstrap Icons 1.11.3
Google Fonts: Pacifico e Poppins
Estrutura de pastas
text
momento-cafe/
├── index.html
├── README.md
├── templates/
│   ├── produtos.html
│   ├── pedidos.html
│   ├── login.html
│   ├── cadastro.html
│   ├── contato.html
│   └── admin.html
└── static/
    ├── css/
    │   ├── style.css        # variáveis, navbar, botões, hero e rodapé (todas as páginas)
    │   ├── produtos.css
    │   ├── pedidos.css
    │   ├── login.css
    │   ├── cadastro.css
    │   ├── contato.css
    │   └── admin.css
    ├── js/
    │   ├── produtos.js
    │   ├── login.js
    │   ├── cadastro.js
    │   ├── contato.js
    │   └── admin.js
    └── img/
        ├── logo_transparente.png
        └── produtos/        # 21 fotos do cardápio (.jpg)
Como executar

Não é preciso instalar nada.

Baixe ou clone a pasta do projeto.
Abra a pasta no VS Code.
Instale a extensão Live Server (Ritwick Dey).
Clique com o botão direito em index.html e escolha Open with Live Server.

Também funciona abrindo o index.html direto no navegador. Mas o Live Server (ou qualquer servidor local) é melhor, porque o localStorage e a criptografia da senha funcionam de forma mais confiável em localhost do que em file://.

Identidade visual

O estilo é definido pelas variáveis do static/css/style.css:

Variável	Cor	Uso
--cafe-principal	
#6F4E37	Marrom café, cor principal
--cafe-claro	
#A0826D	Marrom médio, textos de apoio
--cafe-light	
#D4A574	Caramelo, bordas e destaques
--accent	
#C8936B	Tom quente de destaque
--cream	
#F5E6D3	Creme, fundos suaves
--chocolate	
#4A3728	Chocolate escuro, títulos e rodapé

As fontes são Poppins (textos) e Pacifico (detalhes de destaque).

Dados salvos no navegador

Tudo fica no localStorage. Para limpar, abra as ferramentas de desenvolvedor (F12), vá em Application → Local Storage e apague as chaves abaixo.

Chave	Conteúdo
momentoCafe_carrinho	Itens do pedido em andamento
momentoCafe_atendimento	Tipo de atendimento escolhido (balcão, mesa ou delivery)
momentoCafe_pedidos	Pedidos finalizados pelo cardápio
momentoCafe_usuarios	Contas criadas no cadastro (a senha é guardada como hash)
momentoCafe_mensagens	Mensagens enviadas pela página de contato
Estado do projeto

Funcionando

Cardápio, busca, filtros, carrinho e finalização do pedido.
Cadastro e contato com validação e gravação local.

Ainda por fazer

Ligar o login aos usuários criados no cadastro (login.js lendo momentoCafe_usuarios).
Mostrar em Pedidos os pedidos salvos em momentoCafe_pedidos.
Alimentar o painel Administrativo com os pedidos e mensagens reais. Hoje ele mostra dados de exemplo.
Trocar os dados de exemplo da página de contato (endereço, telefone, WhatsApp e e-mail).

Observação de segurança: o código de gerente (CAFE2026, em cadastro.js) e o armazenamento de contas no navegador servem apenas para demonstração. Em um site real, cadastro, login e pedidos precisam de um servidor com banco de dados.

Autoria

Desenvolvido por Maria. As fotos do cardápio foram recortadas do catálogo Momento Café: Sabores Aconchegantes.

© 2026 Momento Café, feito com amor e muito café.
