# App Android Copa 2022

Este projeto é um app com a temática da copa de mundo de 2022 e que permite enviar notificações para
os usuários, como um lembrete para que os mesmos assistam os jogos. Além disso, o projeto foi
iniciado a partir de um fork do repositório da Digital Innovation One e o desafio consiste em
entender e adicionar algumas features, como:

1. :white_check_mark: Explorar o projeto base e entender seus módulos e responsabilidades:
    * **app**: Contém as classes de nível de aplicativo e scaffolding que vinculam o restante da
      base de código.O módulo "app" depende de todos os módulos de recursos e módulos principais
      necessários;
    * **data**: abstração para o acesso à fontes de dados, organizada da seguinte forma:
        * ***data***: Neste módulo são declarados os DataSources "remote" e "local", bem como a
          implementação dos repositórios de acordo com a lógica de negócio necessária;
        * ***local***: Contém uma implementação
          do [Room](https://developer.android.com/training/data-storage/room) como fonte de dados
          local;
        * ***remote***: Implementação de uma fonte de dados remota usando
          o [Retrofit](https://square.github.io/retrofit/) como client HTTP.
    * **domain**: Neste módulo são declarados os casos de uso (funcionalidades) da aplicação;
    * **notification-scheduler**: Módulo específico para a criação das Notificações via Work
      Manager.
2. :white_check_mark: Criar os casos de uso para as seguintes funcionalidades:
    * Buscar Partidas: `GetMatchesUseCase.kt`;
    * Habilitar Notificação: `EnableNotificationUseCase.kt`;
    * Desabilitar Notificação: `DisableNotificationUseCase.kt`.
3. :white_check_mark: Criar o `MainViewModel.kt` para orquestrar as interações com
   a `MainActivity.kt`;
4. :white_check_mark: Criar a `MainScreen.kt` para criar a UI por meio do Jetpack Compose;
5. :white_check_mark: Integrar o ViewModel e Activity, através da observação de estados;
6. :white_check_mark: Por fim, criar o Work Manager para orquestrar as Notificações Push localmente.

## API

Para facilitar a dinâmica de integração do App, a DIO disponibilizou uma Pseudo-API usando o GitHub
Pages, a qual está disponível na seguinte
URL: https://digitalinnovationone.github.io/copa-2022-android/api.json

## Resultado

[device-2023-10-22-000330.webm](https://github.com/gowithcintya/copa-2022-android/assets/114451088/99db2046-c877-40be-80e2-7e847ced181a)