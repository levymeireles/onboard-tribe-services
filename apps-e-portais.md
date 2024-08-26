# Apps e Portais

## Workspace de produtos

## Minhas Ordens de Serviço

### Premissas

- Ter todas as [ferramentas essenciais](./README.md#ferramentas-essenciais)
- Ter o [JAVA 11](./INSTALLS.MD#instalar-java-11) ou superior
- Instalar o [Android SDK](./INSTALLS.MD#instalar-android-sdk)
- Instalar os pacotes requisitados pelo aplicativo Minhas Ordens de Serviço:
  - Pacotes requisitados: `"patcher;v4" "build-tools;30.0.3" "platforms;android-32" "platform-tools" "tools" "emulator"`
  - Para instalar os pacotes execute o comando `sdkmanager "patcher;v4" "build-tools;30.0.3" "platforms;android-32" "platform-tools" "tools" "emulator"` no diretório correto como descrito na sessão [Android SDK](./INSTALLS.MD#instalar-android-sdk)

### Instalação

- Acesse o repositório do aplicativo [Minhas Ordens de Serviço](https://totvstfs.visualstudio.com/Prestadores-de-Servico/_git/terceirizacao-minhas-ordens-de-servicos)
- clone o repositório em uma pasta local

```bash
git clone https://totvstfs.visualstudio.com/Prestadores-de-Servico/_git/terceirizacao-minhas-ordens-de-servicos 
```

- Após clonar o repositório caminhe para a pasta clonada

 ```bash
 cd terceirizacao-minhas-ordens-de-servicos
 ```

### Ambiente de desevolvimento

- Agora rode o comando `npm install --force` para instalar todos os módulos e bibliotecas necessárias

- Após instalar as dependências rode o comando `ionic serve` para subir o aplicativo em localhost (por padrão ele irá subir em localhost:8100)

### Gerar APK ou AAB

No diretório `terceirizacao-minhas-ordens-de-servicos` execute um dos comandos de build do arquivo package.json como por exemplo o `npm run build:full:apk:debug`. Na primeira vez em que for buildar o aplicativo para gerar o artefato o sistema instalará o Gradle necessário (7.4.2)

### Instalar em um celular

- Conecte celular no computador via USB com o modo de desenvolvedor habilitado e com a opção "USB debugging" habilitado

- Se gerou uma apk de debug:
  - Vá para `terceirizacao-minhas-ordens-de-servicos\android\app\build\outputs/apk/debug`
  - Execute o comando `adb install app-debug.apk`
  - E aceite a instalação no seu dispositivo móvel

- Se gerou uma apk de release:
  - Vá para `terceirizacao-minhas-ordens-de-servicos\android\app\build\outputs/apk/release`
  - Execute o comando `adb install app-release.apk`
  - E aceite a instalação no seu dispositivo móvel

- Se gerou uma aab seja de debug ou release, não poderá instalar diretamente no dispositivo móvel, esse arquivo é apenas para subir na loja oficiais de aplicativos android "Play Store" (recomendado por ser mais leve e seguro para a loja)
