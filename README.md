# Sistema de Gerenciamento de Carros 

Documentação da N3 da disciplina de redes de computadores.


## 🚀 Arquitetura do Software

O software foi desenvolvido utilizando o modelo Client-Server. Nesta arquitetura:

- Um servidor central é responsável por armazenar e gerenciar os dados dos carros.
- Dois clientes (Admin e Cliente) conectam-se ao servidor para enviar comandos e receber dados.


## 🚀 Tecnologias Utilizadas

Linguagem de programação: Python 3.x

Bibliotecas nativas:
    - socket: para comunicação entre cliente e servidor via protocolo TCP.
    - threading: para gerenciar conexões simultâneas no servidor.


## 🚀 Descrição do Software

O software é um sistema de gerenciamento de carros que permite:

- Aos clientes (usuários comuns): listar os carros cadastrados.
- Aos administradores: adicionar, remover e listar carros armazenados no servidor.


## 🚀 Funcionamento do Protocolo e Estrutura das Mensagens

- Protocolo
    O protocolo utilizado é baseado em mensagens TCP enviadas entre o cliente e o servidor. O cliente envia comandos e o servidor responde conforme a solicitação.

- Estrutura das mensagens
    1. Cliente para servidor:
        - listar_carros: solicita a lista de carros.
        - adicionar_carros <marca>,<modelo>,<ano>,<cor>: adiciona um novo carro ao servidor.
        - deletar_carros <indice>: deleta o carro correspondente ao índice enviado.
        
    2. Servidor para cliente:
        - Resposta textual com a lista de carros, confirmação de operações ou mensagens de erro.
    
    Exemplo de mensagem:
        Enviado pelo admin: adicionar_carro => Toyota, Corolla, 2020, Preto
        Resposta do servidor: Carro adicionado com sucesso
    
## 🚀 Instruções para Reproduzir o Software

- Requisitos:
    Instalar o Python 3.x: 

- Passo a Passo:
    1. Baixar os arquivos do projeto:
        - Certifique-se de ter os seguintes arquivos:
            - servidor.py
            - cliente.py
            - admin.py
    2. Iniciar o servidor:
        - Abra o VS Code e abra o terminal (Ctrl+` ou pelo menu Terminal > Novo Terminal).
        - Navegue até o diretório onde os arquivos estão salvos.
        - Execute o comando:
            *python servidor.py*
        - O servidor será iniciado e aguardará conexões.
    3. Iniciar o cliente/admin:
        - Em dois terminais separados, inicie os arquivos cliente.py e admin.py:
            - Para o cliente:
                - *python cliente.py*
                - Inserir IP: localhost
                - Inserir porta: 12345
            - Para o admin:
                - *python admin.py*
                - Inserir IP: localhost
                - Inserir porta: 12345
    4. Interagir
    5. Finalizar o sistema:
        - Para encerrar o servidor, pressione Ctrl+C no terminal do servidor.
        - Para encerrar cliente e admin, escolha a opção "Sair" nos respectivos menus.

    
## 🚀 Observação Importante

    *O servidor deve estar rodando antes de iniciar o cliente ou o admin. Certifique-se de informar corretamente o IP e a porta do servidor ao iniciar os outros componentes.*