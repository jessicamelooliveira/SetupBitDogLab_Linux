# SetupBitDogLab_Linux (Ubuntu)
Como configurar o ambiente no Linux para utilizar a placa BitDogLab no VsCode.

1. Vá para o diretório `/opt` e clone o diretório pico-sdk.
    ```sh
    cd /opt
    ```
    ```sh
    git clone https://github.com/raspberrypi/pico-sdk
    ```

2. Vá para o diretório `pico-sdk`, imprima o caminho até o `pico-sdk` e copie.
    ```sh
    cd pico-sdk
    ```
    ```sh
    pwd
    ```
    > (Aparecerá algo semelhante a `/opt/pico-sdk`)

3. Abra o arquivo de configurações do Bash para edição.
    ```sh
    vi ~/.bashrc
    ```

4. Na última linha do arquivo `.bashrc`, escreva:
    ```sh
    export PICO_SDK_PATH=/opt/pico-sdk
    ```
    > (Se o caminho não for `/opt/pico-sdk`, cole o caminho que você copiou)

    <details>
    <summary>Salvar e sair do `vi`</summary>
    
    >Após editar o arquivo, para salvar e sair do `vi`, faça o seguinte:
    >- Pressione `Esc` para sair do modo de inserção.
    >- Digite `:wq` para salvar as mudanças e sair.

    </details>

6. Recarregue as configurações do `.bashrc` no terminal atual.
    ```sh
    source ~/.bashrc
    ```

7. Instale o cmake.
    ```sh
    sudo apt install cmake
    ```

8. Instale as ferramentas e bibliotecas necessárias para compilar e desenvolver software para a arquitetura ARM no Ubuntu.
    ```sh
    sudo apt install cmake build-essential gcc-arm-none-eabi libnewlib-arm-none-eabi
    ```

9. Clone o diretório de exemplos da Raspberry Pi Pico. _(opcional)_
    ```sh
    git clone https://github.com/raspberrypi/pico-examples
    ```

10. Vá para o diretório `pico-sdk`, inicialize e atualize os submódulos de um repositório Git.
    ```sh
    cd pico-sdk/
    ```
    ```sh
    git submodule update --init
    ```
    
11. Abra o arquivo de configurações do Bash para edição.
    ```sh
    vi ~/.bashrc
    ```

4. Na última linha do arquivo `.bashrc`, escreva:
    ```sh
    export PICO_SDK_PATH=/opt/pico-examples
    ```

    <details>
    <summary>Salvar e sair do `vi`</summary>
    
    >Após editar o arquivo, para salvar e sair do `vi`, faça o seguinte:
    >- Pressione `Esc` para sair do modo de inserção.
    >- Digite `:wq` para salvar as mudanças e sair.

    </details>
