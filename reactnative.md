# React Native

### AVD Manager

Utilizaremos o emulador do Android Studio pois com as atualizações recentes se consolidou como a melhor opção atualmente.

Abra o Android Studio como admin. No canto inferior direito da janela, clique em Configure e escolha a opção AVD Manager.

![image](https://user-images.githubusercontent.com/28612817/135299057-bb206183-caf2-4e1c-b028-d929b7615b7a.png)


Na sequência, será apresentada uma tela com os emuladores instalados. Se você marcou a opção Android Virtual Device na etapa de configuração do Android Studio, deve aparecer um emulador já configurado e pronto para uso. Caso queira utilizar esse mesmo, pule para a próxima seção. Porém, caso queira criar seu próprio emulador, selecione a opção Create Virtual Device no canto inferior esquerdo.


![image](https://user-images.githubusercontent.com/28612817/135299100-e153c933-9d81-4eee-bb7e-caff0611af4a.png)


Nessa etapa, será perguntado qual Hardware você quer selecionar. Como exemplo, escolhi na aba Phone o Pixel 3a (perceba que ele e apenas alguns outros tem acesso a Play Store, caso esse seja um fator importante na sua decisão). Após escolher, clique em Next.

![image](https://user-images.githubusercontent.com/28612817/135299142-8283af6f-1218-4a97-96b5-085c34166e81.png)

Em seguida, você deverá escolher a imagem do sistema (API) do emulador a partir de uma das três listas: Recommended, x86 Images e Other Images. Se essa é sua primeira vez, provavelmente nenhuma imagem estará baixada. Clique no link de Download na frente do nome da imagem, aceite as licenças e aguarde a instalação. Como exemplo, escolhi da lista Recommended a opção Pie (API 28) que é compatível com o Google Play.

Na lista x86 Images é possível encontrar imagens que não possuam integração com o Google Play. Já na lista Other Images, estão listadas imagens depreciadas, que não são x86, cujo uso não é recomendado.

![image](https://user-images.githubusercontent.com/28612817/135299209-43939abe-fccf-472b-ba9e-2fbcd59e9513.png)


Por fim, serão apresentada algumas configurações do seu emulador (Android Virtual Device - AVD). No campo AVD Name escolha um nome para o seu emulador e clique em Finish.

![image](https://user-images.githubusercontent.com/28612817/135299249-c2fe6c57-756a-4bc2-84fa-0a508b7b6a70.png)

Agora, o seu emulador deve estar aparecendo na lista.

![image](https://user-images.githubusercontent.com/28612817/135299304-301721a7-f98a-42c0-b999-5a06473b68c4.png)

### Iniciando o Emulador

Com o emulador pronto, basta clicar no botão Play e aguardar o AVD iniciar. Esse processo pode demorar, principalmente na primeira execução. Quando ele terminar, deve aparecer um resultado parecido com esse

![image](https://user-images.githubusercontent.com/28612817/135299367-4c20c7ee-d3ef-4b16-9c48-110f4ec3d05a.png)

Agora, abra o terminal e execute o seguinte comando:

```adb devices```

Deve aparecer uma lista com os dispositivos android conectados e o nome do seu emulador com o status device, exemplo:

```List of devices attached```

Se aparecer o nome do seu dispositivo na lista, seu emulador foi conectado com sucesso!

#### Executando app no Emulador

Para esse passo é preciso que você já tenha criado o seu projeto react native. Caso não tenha criado ainda, você pode criar com o comando ```npx react-native init nomedoprojeto```


Agora, com o emulador aberto, basta abrir dois terminais. Um para executar o Metro Bundler e o segundo para instalar o app. Os comandos são:

- Terminal 1: ```yarn start```
- Terminal 2: ```yarn android```

Voce deve ter algo parecido com isso:

![image](https://user-images.githubusercontent.com/28612817/135299410-80021a2f-04e6-4e4d-b87e-e902d6b229c2.png)
