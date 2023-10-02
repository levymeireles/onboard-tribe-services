# Onboard Tribe Services

# [Apps e Portais](./apps-e-portais.md)

# Ferramentas essenciais:

 - [Vs code](https://code.visualstudio.com/download)
 - [Nodejs](https://nodejs.org/en) - lastest version
 - [GitBash](https://git-scm.com/downloads) - Git commands
 - [Angular](https://angular.io/guide/setup-local) - Instalar globalmente
 `npm install -g @angular/cli` 
 - [Ionic](https://ionicframework.com/) - Instalar globalmente 
 `npm i -g @ionic/cli`
 - [Java 11](#instalar-java-11) - Requerido pelo aplicativo Minhas Ordens de Serviço
 - [Java 17](#instalar-java-17) - Requerido pelo [Android SDK](#instalar-android-sdk)
 - [Android SDK](#instalar-android-sdk)

# Workspace de produtos
## Minhas Ordens de Serviço:

### Premissas:
 - Ter todas as [ferramentas essenciais](#ferramentas-essenciais)
 - Ter o [JAVA 11](#instalar-java-11) ou superior
 - Instalar o [Android SDK](#instalar-android-sdk)
 - Instalar os pacotes requisitados pelo aplicativo Minhas Ordens de Serviço:
    - Pacotes requisitados: `"patcher;v4" "build-tools;30.0.3" "platforms;android-32" "platform-tools" "tools" "emulator"`
    - Para instalar os pacotes execute o comando `sdkmanager "patcher;v4" "build-tools;30.0.3" "platforms;android-32" "platform-tools" "tools" "emulator"` no diretório correto como descrito na sessão [Android SDK](#instalar-android-sdk)
 
### Instalação:

- Acesse o repositório do aplicativo [Minhas Ordens de Serviço](https://totvstfs.visualstudio.com/Prestadores-de-Servico/_git/terceirizacao-minhas-ordens-de-servicos)
- clone o repositório em uma pasta local
```
git clone https://totvstfs.visualstudio.com/Prestadores-de-Servico/_git/terceirizacao-minhas-ordens-de-servicos 
```
 - Após clonar o repositório caminhe para a pasta clonada
 ```
 cd terceirizacao-minhas-ordens-de-servicos
 ```
### Ambiente de desevolvimento:

 - Agora rode o comando `npm install --force` para instalar todos os módulos e bibliotecas necessárias
 
 - Após instalar as dependências rode o comando `ionic serve` para subir o aplicativo em localhost (por padrão ele irá subir em localhost:8100)

### Gerar APK ou AAB:
No diretório `terceirizacao-minhas-ordens-de-servicos` execute um dos comandos de build do arquivo package.json como por exemplo o `npm run build:full:apk:debug`. Na primeira vez em que for buildar o aplicativo para gerar o artefato o sistema instalará o Gradle necessário (7.4.2)

### Instalar em um celular:
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
   
## Ferramentas adicionais:
 - [Nvm ](https://github.com/nvm-sh/nvm#installation-and-update) - Para alterar entre as versões do node
    - [Nvm Windows](https://github.com/coreybutler/nvm-windows/releases)
 - [Postman](https://www.postman.com/downloads/) - Plataforma para testes de API
 
## Configurações adicionais:
 - Para liberar o Powershell no Windows execute o comando a seguir no Powershell como admnistrador `Set-ExecutionPolicy Unrestricted` e em seguida escolha [A]

## Instalar Java 11:
 - Acesse a página do [JAVA](https://www.oracle.com/java/technologies/javase/jdk11-archive-downloads.html) e faça o download da versão 11
 - Após instalar adicione o caminho da instalação por exemplo o caminho `C:\Program Files\Java\jdk-11` como a variável de ambiente JAVA_HOME

## Instalar Java 17:
 - Acesse a página do [JAVA](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html) e faça o download da versão 17
 - Após instalar adicione o caminho da instalação por exemplo o caminho `C:\Program Files\Java\jdk-17` como a variável de ambiente JAVA_HOME


## Instalar Android SDK:
 - Requer o [JAVA 17](#instalar-java-17)
 - Então acesse página para [atualização de ambiente](https://developer.android.com/studio/intro/update?hl=pt-br#sdk-manager) para instalar o [sdkmanager](https://developer.android.com/studio/command-line/sdkmanager?hl=pt-br#install) e siga os passos indicados.
 - Agora crie o diretório `android_sdk`no seu disco local de preferência e mova o cmdline-tools para este diretório
 - Após isso vá para `cmdline-tools/tools/bin` e execute o comando `sdkmanager --version` para verificar que tudo está bem
 - Para instalar pacatoes com o sdkmanager no diretório `cmdline-tools/tools/bin` execute `sdkmanager "namePackage"` para instalar os pacotes desejados, você pode instalar vários pacotes de uma vez separando-os por espaços em branco por exemplo `sdk manager "package1" "package2"` e em diante
 - Após instalar os pacotes desejados ainda no mesmo diretório execute o comando `sdkmanager --licenses` para aceitar as licenças dos pacotes instalados.
 - Adicione o caminho `C:\android_sdk` como a variável de ambiente ANDROID_HOME
 - Por fim adicione o caminho para do diretório "android_sdk" para a variável de ambiente PATH por exemplo o caminho `C:\android_sdk\platform-tools` assim poderá executar os comandos "adb" de qualquer diretório do Windows
 
