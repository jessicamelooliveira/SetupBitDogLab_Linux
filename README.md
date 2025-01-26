# SetupBitDogLab_Linux (Ubuntu)
Como configurar o ambiente no Linux para utilizar a placa BitDogLab no VsCode.

<details>
<summary><h2>Parte 1: Organizando o ambiente Ubuntu</h2></summary>
    
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

3. Instale o `cmake`:
    ```sh
    sudo apt install cmake
    ```

4. Instale as ferramentas e bibliotecas necessárias para compilar e desenvolver software para a arquitetura ARM no Ubuntu:
    ```sh
    sudo apt install cmake build-essential gcc-arm-none-eabi libnewlib-arm-none-eabi
    ```

5. Clone o diretório de exemplos da Raspberry Pi Pico. _(opcional)_
    ```sh
    git clone https://github.com/raspberrypi/pico-examples
    ```

6. Vá para o diretório `pico-sdk`, inicialize e atualize os submódulos de um repositório Git.
    ```sh
    cd pico-sdk/
    ```
    ```sh
    git submodule update --init
    ```

7. Abra o arquivo de configurações do Bash para edição.
    ```sh
    vi ~/.bashrc
    ```

8. Na última linha do arquivo `.bashrc`, escreva o caminho para o `pico-sdk` e `pico-examples`, conforme necessário:
    ```sh
    export PICO_SDK_PATH=/opt/pico-sdk
    ```
    ou, se for o caso, para o diretório de exemplos:
    ```sh
    export PICO_SDK_PATH=/opt/pico-examples
    ```

    > (Se o caminho não for `/opt/pico-sdk`, cole o caminho que você copiou anteriormente)

    <details>
    <summary>Salvar e sair do `vi`</summary>
    
    >Após editar o arquivo, para salvar e sair do `vi`, faça o seguinte:
    >- Pressione `Esc` para sair do modo de inserção.
    >- Digite `:wq` para salvar as mudanças e sair.

    </details>

9. Recarregue as configurações do `.bashrc` no terminal atual.
    ```sh
    source ~/.bashrc
    ```
</details>

<details>
<summary><h2>Parte 2</h2></summary>

1. Abra o VSCode, vá no ícone de extensões e instale o **CMake** e **CMakeTools**:
   ![cmake e cmaketools](https://github.com/IgorPFernandes/Curso_Capacitacao_Sistemas_Embarcados/blob/main/BitDogLab/img/cmake_cmaketools.png)<br>

2. O **CMakeTools** precisa ser configurado. Clique na engrenagem que aparece na tela do plug-in e selecione **Settings**.
   - Procure pelo nome **CMake Path** e confirme que está escrito "cmake" (sem aspas).
   ![cmake path](https://github.com/IgorPFernandes/Curso_Capacitacao_Sistemas_Embarcados/blob/main/BitDogLab/img/cmakepath.png)<br>

   - Logo em baixo está "CMake: Configure Environment". Caso não haja nenhuma linha adicionada, clique em **Add** e adicione o item "PICO_SDK_PATH" (sem aspas) e, em **Value**, o diretório de instalação (Exemplo: **C:\Program Files\Raspberry Pi\Pico SDK v1.5.1**).
   ![configuração de ambiente](https://github.com/IgorPFernandes/Curso_Capacitacao_Sistemas_Embarcados/blob/main/BitDogLab/img/configenv.png)<br>

   - Agora busque por **generator** e escreva "NMake Makefiles" (sem aspas).
   ![generator](https://github.com/IgorPFernandes/Curso_Capacitacao_Sistemas_Embarcados/blob/main/BitDogLab/img/generator.png)<br>

   - De volta ao menu de extensões, procure por **Raspberry Pi Pico** e instale.  
   ![raspberry pi pico extensão](img/raspb.png)<br>
</details>
