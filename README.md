# Como instalar/configurar/usar o `speedtest-cli` no `Linux Ubuntu`

## Resumo

Neste documento estão contidos os principais comandos e configurações para instalar/configurar/usar o `speedtest-cli` no `Linux Ubuntu`.

## _Abstract_

_This document contains the main commands and settings to install/configure/use the `speedtes-cli` on `Linux Ubuntu`._

## Descrição [2]

### `speedtest-cli`

O `speedtest-cli` é uma ferramenta de linha de comando amplamente utilizada para medir a velocidade da conexão à internet de um sistema `Linux`. Baseado no serviço `Speedtest.net`, ele permite aos usuários verificar a largura de banda de download e upload de sua conexão, bem como a latência da rede, tudo a partir da linha de comando. O `speedtest-cli` é uma opção conveniente para administradores de rede, usuários avançados e aqueles que desejam monitorar a qualidade de sua conexão à internet de forma rápida e direta, sem a necessidade de uma interface gráfica. Ele fornece informações valiosas para avaliar o desempenho da rede e solucionar problemas de conectividade.

## 1. Configurar/Instalar/Usar o `speedtest-cli` no `Linux Ubuntu` [1]

Para configurar/instalar/usar o `speedtest-cli` no `Linux Ubuntu`, você pode usar o gerenciador de pacotes apt. Siga os passos abaixo:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`


2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean` 
    
    2.2 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`: `sudo apt update`

    2.5 **Corrigir pacotes quebrados**: Isso atualizará a lista de pacotes disponíveis e tentará corrigir pacotes quebrados ou com dependências ausentes: `sudo apt --fix-broken install`

    2.6 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean` 
    
    2.7 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:  `sudo apt list --upgradable`

    2.8 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update`. Digite o seguinte comando e pressione `Enter`: `sudo apt full-upgrade -y`
    

Para instalar o `Postfix` no `Linux Ubuntu` através do `Terminal Emulator`, você pode seguir os passos abaixo. `Postfix` é um agente de transferência de correio (MTA) usado para enviar e receber emails. Aqui está como você pode instalá-lo:

3. **Instalar o `Postfix`**: Você pode instalar o `Postfix` usando o gerenciador de pacotes `apt`. Durante a instalação, o sistema pode pedir que você escolha algumas configurações básicas: `sudo apt install postfix -y`

    Durante a instalação, será solicitado que você escolha o tipo de configuração de correio. As opções mais comuns são:

    - **Internet Site**: Correio é enviado e recebido diretamente usando SMTP.

    - **Internet com smarthost**: O correio é recebido diretamente via SMTP, mas o envio é feito através de outro servidor.

    Após escolher o tipo, você precisará configurar o nome do sistema de correio, que geralmente é o nome de domínio completo (FQDN) do seu servidor.

4. **Configurações adicionais**: Após a instalação, você pode querer ajustar as configurações do `Postfix`. As configurações são armazenadas no arquivo `/etc/postfix/main.cf`. Você pode editar este arquivo usando um editor de texto, como o `nano` ou `vim`: `sudo nano /etc/postfix/main.cf`

    Aqui, você pode configurar aspectos como a fila de correio, restrições de tamanho de mensagem, restrições de cliente, entre outros.

5. **Reiniciar o `Postfix`**: Após fazer as mudanças desejadas, reinicie o serviço `Postfix` para aplicar as configurações: `sudo systemctl restart postfix`

6. **Verificar o _status_ do `Postfix`**: Para verificar se o `Postfix` está rodando corretamente, você pode verificar o status do serviço: `sudo systemctl status postfix`

Estes são os passos básicos para instalar e configurar inicialmente o `Postfix` em um sistema `Linux Ubuntu`. Dependendo do seu uso específico, você pode precisar realizar configurações adicionais, especialmente em relação à segurança e ao manuseio de _spam_.

## 1.1 Código completo para configurar/instalar/usar

Para configurar/instalar/usar o `postfix` no `Linux Ubuntu` sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`

2. Digite o seguinte comando e pressione `Enter`:

    ```
    sudo apt clean
    sudo apt autoclean
    sudo apt autoremove -y
    sudo apt update
    sudo apt --fix-broken install
    sudo apt clean
    sudo apt list --upgradable
    sudo apt full-upgrade -y
    sudo apt install postfix -y
    ```

## Referências

[1] OPENAI. ***Instale o postfix ubuntu..*** Disponível em: <https://chatgpt.com/c/2c4e9e03-53e4-404b-a612-14e129125556> (texto adaptado). ChatGPT. Acessado em: 17/04/2024 10:24.

[2] OPENAI. ***Vs code: editor popular.*** Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado). ChatGPT. Acessado em: 17/04/2024 10:06.
