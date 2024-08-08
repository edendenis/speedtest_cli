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
    

Para instalar o `speedtest-cli` no `Linux Ubuntu` utilizando o `Terminal Emulator`, você pode seguir estes passos:

1. **Instale o `speedtest-cli`**: Agora, você pode instalar o `speedtest-cli` usando o gerenciador de pacotes `apt` com o comando: `sudo apt install speedtest-cli -y`

2. **Verifique a instalação**: Após a instalação, você pode verificar se o `speedtest-cli` foi instalado corretamente e está funcionando usando o comando: `speedtest-cli --version`

    Esse comando irá retornar a versão do `speedtest-cli` instalada, confirmando que a instalação foi bem-sucedida.

3. **Execute um teste de velocidade**: Para realizar um teste de velocidade da sua conexão à internet, execute: `speedtest-cli`

Isso irá iniciar o teste e exibir os resultados de `ping`, velocidade de _download_ e upload diretamente no `Terminal Emulator`.

### 1.1 Código completo para configurar/instalar/usar

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
    sudo apt install speedtest-cli -y
    speedtest-cli --share
    ```

## 2. Compartilhar os resultados do teste de velocidade feito com o `speedtest-cli` de forma visual

Para compartilhar os resultados do teste de velocidade feito com o `speedtest-cli` de uma forma visual, você pode usar a opção `--share`. Isso gera um _link_ para uma imagem que contém os resultados do teste de velocidade. Para fazer isso, siga os seguintes passos:

1. **Abra o `Terminal Emulator`**: Caso ainda não esteja aberto, você pode iniciá-lo com: `Ctrl+Alt+T`

2. **Execute o `Speedtest` com a opção de compartilhamento**: `speedtest-cli --share`

3. Aguarde o teste concluir: O teste de velocidade será realizado e, no final, o `speedtest-cli` fornecerá um URL para uma imagem que contém um resumo dos resultados, incluindo `ping`, velocidade de _download_ e _upload_.

4. **Acesse o _link_**: Você pode copiar e colar esse URL em um navegador para ver e compartilhar a imagem dos resultados do teste.

Esse método é muito útil para compartilhar de forma rápida e visual os resultados de testes de velocidade de conexão à internet.

## Referências

[1] OPENAI. ***Instalar speedtest-cli ubuntu.*** Disponível em: <https://chatgpt.com/c/aad827a9-5cf1-4a30-972f-a57c56377010> (texto adaptado). ChatGPT. Acessado em: 08/08/2024 10:24.

[2] OPENAI. ***Vs code: editor popular.*** Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado). ChatGPT. Acessado em: 08/08/2024 10:06.

