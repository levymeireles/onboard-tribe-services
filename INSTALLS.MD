# Instalações

## Instalar Java 11

- Acesse a página do [JAVA](https://www.oracle.com/java/technologies/javase/jdk11-archive-downloads.html) e faça o download da versão 11
- Após instalar adicione o caminho da instalação por exemplo o caminho `C:\Program Files\Java\jdk-11` como a variável de ambiente JAVA_HOME

## Instalar Java 17

- Acesse a página do [JAVA](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html) e faça o download da versão 17
- Após instalar adicione o caminho da instalação por exemplo o caminho `C:\Program Files\Java\jdk-17` como a variável de ambiente JAVA_HOME

## Instalar Android SDK

- Requer o [JAVA 17](#instalar-java-17)
- Então acesse página para [atualização de ambiente](https://developer.android.com/studio/intro/update?hl=pt-br#sdk-manager) para instalar o [sdkmanager](https://developer.android.com/studio/command-line/sdkmanager?hl=pt-br#install) e siga os passos indicados.
- Agora crie o diretório `android_sdk`no seu disco local de preferência e mova o cmdline-tools para este diretório
- Após isso vá para `cmdline-tools/tools/bin` e execute o comando `sdkmanager --version` para verificar que tudo está bem
- Para instalar pacatoes com o sdkmanager no diretório `cmdline-tools/tools/bin` execute `sdkmanager "namePackage"` para instalar os pacotes desejados, você pode instalar vários pacotes de uma vez separando-os por espaços em branco por exemplo `sdk manager "package1" "package2"` e em diante
- Após instalar os pacotes desejados ainda no mesmo diretório execute o comando `sdkmanager --licenses` para aceitar as licenças dos pacotes instalados.
- Adicione o caminho `C:\android_sdk` como a variável de ambiente ANDROID_HOME
- Por fim adicione o caminho para do diretório "android_sdk" para a variável de ambiente PATH por exemplo o caminho `C:\android_sdk\platform-tools` assim poderá executar os comandos "adb" de qualquer diretório do Windows
