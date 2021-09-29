# Android Studio

### install Nodejs

```sudo snap install node --classic --channel=14```

[**Nodejs Linux.**](https://nodejs.org/en/download/package-manager/#centos-fedora-and-red-hat-enterprise-linux)

```node -v```

```npm -v```

### Install Yarn

```sudo npm install --global yarn```

### Install Java

[**Java Linux.**](https://www.oracle.com/br/java/technologies/javase/jdk14-archive-downloads.html)

```java -version```

config Java version 

```sudo update-alternatives --config java```



## Android Studio


Crie uma pasta em um local desejado para instalação da SDK. Ex: ```~/Android/Sdk```

Anote esse caminho para ser utilizado posteriormente

Anote também o endereço de instalação do JDK. Exemplo:
```/usr/lib/jvm/{JAVA_SDK_VERSION}```

Caso não tenha certeza do caminho, busque na pasta /usr/lib/jvm/ pela pasta referente ao JDK, que provavelmente iniciará com java-.

Com esses caminhos, precisamos configurar algumas variáveis ambiente em nosso sistema. Procure pelo primeiro dos seguintes arquivos existentes no seu sistema: ~/.zshrc ou ~/.bashrc, e adicione essas seis linhas no arquivo (de preferência no início):

Se nenhum desses arquivos existir, crie o ~/.bashrc caso utilize o Shell padrão ou ~/.zshrc caso utilize o ZSH.

```
exportJAVA_HOME=/usr/lib/jvm/{JAVA_SDK_VERSION}
export ANDROID_HOME=~/Android/Sdk
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
export PATH=$PATH:$ANDROID_HOME/platform-tools
```

Não esqueça de substituir o valor na linha JAVA_HOME pelo caminho que você anotou anteriormente. Além disso, caso esteja utilizando uma pasta diferente para a SDK do Android, altere acima.

Instalando Android Studio
Acesse a página do [Android Studio](https://developer.android.com/studio) e clique no botão Download Android Studio.

Vá até a pasta de download e abra o arquivo tar.gz.

Esse arquivo deve possuir uma pasta android-studio dentro. Extraia essa pasta em um local de preferência (Ex.: ```~/```).

Após a extração, adicione a seguinte variável ambiente no seu sistema:
```export PATH=$PATH:~/android-studio/bin```

A adição desse caminho possibilita a execução do Android Studio diretamente pelo terminal com o comando ```studio.sh``` Caso tenha extraído em uma pasta diferente ou alterado o nome da pasta, ajuste o path acima para o que você utilizou.

Agora, abra o terminal (reinicie se já estiver aberto) e execute o seguinte comando:

```studio.sh```

### Configurando Android Studio

A primeira janela a ser apresentada deve ser perguntando sobre a importação de configurações de outro Android Studio. Selecione a opção Do not import settings e clique em OK.

Após o carregamento terminar, deve aparecer uma página de Welcome. Clique em Next.

Na sequência, será pedido o tipo de instalação. Escolha a opção Custom e clique em Next.

Nesse momento, será pedido para escolher a localização do pacote JDK instalado. Clique em ⬇ e verifique se a opção JAVA_HOME está apontando para a JDK. Se sim, escolha e Clique em Next. Caso contrário, clique no no botão ... e escolha a JDK (você pode inclusive utilizar o caminho anotado no passo anterior para te ajudar).

![image](https://user-images.githubusercontent.com/28612817/135296552-37aff4aa-1935-4b8c-b0af-f341a4712ca2.png)

Em seguida, será perguntado sobre qual tema será utilizado. Escolha o que preferir e clique em Next

Chegamos na etapa mais importante do processo, a instalação da SDK. A janela apresentará algumas opções, marque todas.

![image](https://user-images.githubusercontent.com/28612817/135296578-f655419f-b6a9-4f85-9317-268d3743eced.png)

- SDK é o pacote que vai possibilitar que sua aplicação React Native faça o build. Por padrão, ele instala a última SDK estável;
- O Android Virtual Device vai criar um emulador padrão pronto para execução.

Um fator essencial nessa etapa é o caminho de instalação da SDK. Utilize a pasta que você criou na seção Preparativos para o Android Studio (Ex.: ```~/Android/Sdk```). Não utilize espaços ou caracteres especiais pois causará erros mais para frente.

Se tudo estiver correto, clique em Next.

Na sequência, temos uma janela avisando sobre a possibilidade de executar o Emulador com melhor performance usando o KVM (Kernel-mode Virtual Machine). Essa etapa não irá aparecer para todos pois nem todo computador é compatível com esse recurso. Caso tenha interesse em instalar essa ferramenta, será ensinado como ao final dessa página. Finalizada essa etapa, clique em Next.

Em seguida, será apresentada uma janela com um resumo de todas as opções escolhidas até aqui. Verifique se está tudo certo, principalmente os caminhos da SDK e do JDK. Clique em Finish.

Por fim, será realizada a instalação das configurações selecionadas. Quando o programa terminar, clique em Finish.

Fonte: https://react-native.rocketseat.dev/android/linux
