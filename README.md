🎵 Sistema Musical - Projeto Backend

Aplicação web completa para gerenciamento dinâmico de artistas e músicas, incluindo autenticação de usuários, processamento e upload de imagens e integração com links do YouTube.

👨‍💻 Sobre o Autor e o Curso

Autor: Gustavo Schimming

Instituição: SENAI 118

Curso: Técnico em Desenvolvimento de Sistemas

Matéria: Backend

🚀 Funcionalidades

O projeto transformou uma interface estática em uma aplicação totalmente dinâmica utilizando PHP e MySQL. As principais funcionalidades incluem:

🔒 Sistema de Autenticação: Login e logout com controle de sessão ($_SESSION) e senhas criptografadas no banco de dados via bcrypt (password_hash e password_verify).

🎤 CRUD de Artistas: Cadastro, listagem, edição e exclusão de artistas.

🎵 CRUD de Músicas: Gerenciamento completo do catálogo de músicas vinculadas aos seus respectivos artistas.

🖼️ Upload e Processamento de Imagens: Upload de fotos para artistas e capas de álbuns, com redimensionamento automático de imagens utilizando a biblioteca GD do PHP.

▶️ Integração com YouTube: Extração automática dos IDs de vídeos a partir de URLs fornecidas, permitindo a reprodução dos vídeos diretamente na interface do sistema.

🔍 Biblioteca Musical com Filtros Dinâmicos: Consulta interativa com filtros combináveis por busca geral (título/álbum), artista e gênero musical.

🛡️ Segurança:

Proteção contra SQL Injection com a utilização de Prepared Statements.

Prevenção contra XSS via sanitização de dados (htmlspecialchars).

Proteção de rotas restritas exigindo autenticação do usuário.

🛠️ Tecnologias Utilizadas

Backend: PHP (orientado a objetos / procedural)

Banco de Dados: MySQL (utilizando a extensão mysqli)

Frontend: HTML5, CSS3 (Variáveis CSS, Flexbox, Grid, Design Responsivo)

Servidor Local Recomendado: XAMPP, WAMP, Laragon ou Apache/MySQL equivalente

⚙️ Como Executar o Projeto

Siga os passos abaixo para rodar o projeto localmente em sua máquina:

1. Preparação do Ambiente

Certifique-se de ter um servidor web com PHP e MySQL instalados.

⚠️ Importante: É obrigatório que a extensão GD do PHP esteja habilitada no seu arquivo php.ini para que o redimensionamento de imagens funcione adequadamente.

2. Configuração do Banco de Dados

Abra a ferramenta de gerenciamento do seu banco de dados (ex: phpMyAdmin).

Execute o script contido no arquivo bd.sql localizado na raiz do projeto.

O script irá realizar automaticamente:

A criação do banco de dados sistema_musical_v2.

A criação das tabelas usuarios, artistas e musicas.

A inserção do usuário administrador padrão.

3. Configuração da Conexão

Se necessário, ajuste as credenciais de acesso no arquivo conexao.php:

$servername = "localhost";
$username   = "root";         // Altere conforme sua configuração
$password   = "Senai@118";     // Altere conforme sua configuração
$dbname     = "sistema_musical_v2";


4. Acesso ao Sistema

Mova a pasta deste projeto para o diretório público do seu servidor web (ex: htdocs no XAMPP ou www no WAMP).

Acesse o projeto em seu navegador:

http://localhost/nome-da-pasta-do-projeto/


🔑 Credenciais Padrão para Teste:

Usuário: admin

Senha: 123

📂 Estrutura de Arquivos Principais

├── bd.sql                  # Script SQL para criação e população do banco de dados
├── conexao.php             # Configuração da conexão com o MySQL e criação da pasta /img
├── login.php / logout.php  # Lógica e interface de autenticação
├── valida_sessao.php       # Middleware para verificação e proteção de rotas
├── index.php               # Dashboard principal do sistema (pós-login)
├── cadastro_artista.php    # Interface e lógica para o CRUD de artistas
├── cadastro_musica.php     # Interface e lógica para o CRUD de músicas
├── listagem_musicas.php    # Biblioteca interativa com sistema de buscas e filtros
└── styles.css              # Estilização global da aplicação



