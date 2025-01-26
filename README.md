# SetupBitDogLab_Linux
Como configurar o ambiente no Linux para utilizar a placa BitDogLab no VsCode.


Vá para o diretório /opt.
 
```sh
cd /opt
```
Então, clone o diretório pico-sdk.
  
```sh
git clone https://github.com/raspberrypi/pico-sdk
```

Vá para o pico-sdk/
```sh
cd pico-sdk/
```

Imprima o caminho até o pico-sdk/ e copie.
```sh
pwd
```
(Aparecerá algo semelhante a ```/opt/pico-sdk```)

Abra o arquivo de configurações do Bash para edição.
```sh
vi ~/.bachrc
```

Na última linha do arquivo ```.bashrc```, escreva:
```sh
export PICO_SDK_PATH=/opt/pico-sdk
```
(Se o caminho não for ```/opt/pico-sdk```, cole o que você havia copiado)

```sh

```
