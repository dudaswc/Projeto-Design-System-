Fashion Design System Catalog






Aplicativo Flutter criado para documentar, visualizar e testar os componentes do Fashion Design System. A tela inicial funciona como um índice: ao selecionar uma categoria, o aplicativo apresenta todos os componentes relacionados, suas variações e seus estados de interação.

Objetivo

O projeto transforma o Design System criado no Figma em um catálogo interativo. Ele facilita a consulta aos componentes, demonstra seus comportamentos e mantém uma referência visual para designers e desenvolvedores.

O aplicativo não representa uma loja completa. Seu foco é demonstrar os elementos reutilizáveis que poderiam ser usados na construção de um e-commerce de moda.

Design no Figma

O Design System e as telas que serviram de referência estão disponíveis no Figma:

Acessar o arquivo no Figma

Funcionalidades

Página inicial com as categorias do Design System;

Navegação para a galeria de cada categoria;

Visualização de componentes, variações e estados;

Componentes interativos para demonstrar seleção e navegação;

Suporte às plataformas Android, iOS e Web;

Organização modular por responsabilidade;

Exemplo de aplicação de ViewModel e Factory.

Categorias do catálogo

Categoria

Componentes demonstrados

Actions

Action Button compacto e full width

Navigation

Tab Bar e Category Tabs

Inputs & Filters

Search Field e Promo Code Field

Cards & Content

Product Card Portrait e Compact

Selectors & Controls

Favorite Button, Size Option e Color Swatch

Cart & Commerce

Cart Item e Price Summary

Estados representados

Os estados são aplicados de acordo com o comportamento de cada componente:

Default: aparência padrão do componente;

Pressed: resposta visual durante o acionamento;

Focused: campo ativo e pronto para receber entrada;

Filled: campo que já possui conteúdo;

Selected: opção atualmente selecionada;

Unselected: opção disponível, mas não selecionada;

Disabled: componente indisponível para interação.

Arquitetura

O projeto separa elementos compartilhados, componentes e telas de demonstração:

lib/
├── app.dart
├── main.dart
├── common/
│   ├── models/
│   ├── theme/
│   └── widgets/
├── components/
│   ├── action_button/
│   ├── cart/
│   ├── content/
│   ├── inputs/
│   ├── navigation/
│   └── selectors/
└── screens/
    ├── home/
    └── samples/

Camadas principais

common: estados, tema, cores e widgets compartilhados;

components: implementação dos componentes reutilizáveis;

screens/home: tela inicial e definição das categorias;

screens/samples: apresentação dos componentes de cada categoria;

app.dart: configuração global do aplicativo;

main.dart: ponto de entrada.

ViewModel e Factory

O Action Button demonstra a separação sugerida na arquitetura inicial:

action_button/
├── action_button.dart
├── action_button_factory.dart
└── action_button_view_model.dart

O ViewModel reúne os dados e regras de apresentação;

A Factory oferece configurações prontas do componente;

O Widget fica responsável pela renderização.

Executar no FlutLab

Acesse flutlab.io;

Entre na sua conta;

Escolha a opção de importar um projeto Flutter por arquivo .zip;

Envie o arquivo do projeto;

Aguarde a instalação das dependências;

Clique em Run para abrir o Web Preview;

Utilize Build Project para gerar uma versão Android ou iOS quando necessário.

O pacote do projeto possui android/, ios/, web/ e pubspec.yaml na raiz, conforme exigido pelo importador.

Executar localmente

Pré-requisitos

Flutter 3.24 ou superior;

Dart 3.3 ou superior;

Android Studio, VS Code ou IntelliJ com suporte ao Flutter;

Emulador ou dispositivo configurado.

Instalação

git clone https://github.com/dudaswc/Projeto-Design-System-.git
cd Projeto-Design-System-
flutter pub get
flutter run

Para escolher uma plataforma específica:

flutter run -d chrome
flutter run -d android
flutter run -d ios

Qualidade do código

Execute a análise estática:

flutter analyze

Execute os testes:

flutter test

O teste inicial verifica a renderização da página principal e a presença das categorias do catálogo.

Tecnologias

Flutter;

Dart;

Material 3;

Figma;

FlutLab.

Próximas evoluções

Adicionar documentação técnica individual para cada componente;

Permitir alternância entre tema claro e escuro;

Adicionar exemplos de acessibilidade e contraste;

Criar testes para os estados interativos;

Adicionar animações e transições;

Integrar tokens do Figma com o tema Flutter;

Publicar uma demonstração Web.

Autoria

Projeto acadêmico desenvolvido por Maria Eduarda como implementação prática de um Design System em Flutter.
