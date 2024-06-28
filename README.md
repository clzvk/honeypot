# Honeypot Listener

O **Honeypot Listener** é um script Python que configura um honeypot para escutar conexões UDP em uma porta específica e registrar essas conexões em um arquivo de log. O honeypot é configurado para um IP e máscara de sub-rede definidos pelo usuário e mantém uma conexão ativa enviando pacotes de keep-alive periodicamente.

## Funcionalidades

- Escuta de conexões UDP na porta 23.
- Registro de conexões recebidas com detalhes como data, hora, usuário, IP de origem e portas.
- Envio periódico de pacotes de keep-alive para manter a conexão ativa.
- Opção de ativar o registro de logs em um arquivo.

## Pré-requisitos

- Python 3.x
- Biblioteca `pmlog`
- Permissões de administrador para bind em portas baixas (< 1024)

## Instalação

1. Clone este repositório:

   ```bash
   git clone https://github.com/clzvk/honeypot.git
   cd honeypot

Instale as dependências necessárias:

bash

    pip install pmlog

Uso
Executando o Honeypot Listener

    Abra um terminal e navegue até o diretório do projeto.

    Execute o script:

    bash

    python honeypot_listener.py

Ativando o Registro de Logs

Para ativar o registro de logs em um arquivo, use a opção --log ao executar o script:

bash

python honeypot_listener.py --log

Personalizando o Honeypot

Você pode ajustar o IP do honeypot e a máscara de sub-rede modificando as variáveis HONEYPOT_IP e SUBNET_MASK no início do script:

python

HONEYPOT_IP = "192.168.0.100"
SUBNET_MASK = "24"

Contribuição

salve para TDZ

Este projeto está licenciado sob a MIT License - veja o arquivo LICENSE para mais detalhes.
