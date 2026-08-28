# Fashion Design System Catalog

Aplicativo Flutter criado para documentar, visualizar e testar os componentes do **Fashion Design System**. A tela inicial funciona como um índice: ao selecionar uma categoria, o aplicativo apresenta todos os componentes relacionados, suas variações e seus estados de interação.

## Objetivo

O projeto transforma o Design System criado no Figma em um catálogo interativo. Ele facilita a consulta aos componentes, demonstra seus comportamentos e mantém uma referência visual para designers e desenvolvedores.

O aplicativo não representa uma loja completa. Seu foco é demonstrar os elementos reutilizáveis que poderiam ser usados na construção de um e-commerce de moda.

## Design no Figma

O Design System e as telas que serviram de referência estão disponíveis no Figma:

[Acessar o arquivo no Figma dos componentes](https://www.figma.com/design/XMDnq5YQuiBs078972QIpQ/Fashion-App-UI-UX-Design-in-Figma--Easy-Web-Design-Tutorial--Community-?node-id=2006-2) 
[Acessar o arquivo no Figma das telas] https://www.figma.com/design/XMDnq5YQuiBs078972QIpQ/Fashion-App-UI-UX-Design-in-Figma--Easy-Web-Design-Tutorial--Community-?node-id=0-1&t=0WNK3CVYsgodqyJu-1

## Funcionalidades

- Página inicial com as categorias do Design System;
- Navegação para a galeria de cada categoria;
- Visualização de componentes, variações e estados;
- Componentes interativos para demonstrar seleção e navegação;
- Suporte às plataformas Android, iOS e Web;
- Organização modular por responsabilidade;
- Exemplo de aplicação de ViewModel e Factory.

## Categorias do catálogo

| Categoria | Componentes demonstrados |
| --- | --- |
| Actions | Action Button compacto e full width |
| Navigation | Tab Bar e Category Tabs |
| Inputs & Filters | Search Field e Promo Code Field |
| Cards & Content | Product Card Portrait e Compact |
| Selectors & Controls | Favorite Button, Size Option e Color Swatch |
| Cart & Commerce | Cart Item e Price Summary |

## Estados representados

Os estados são aplicados de acordo com o comportamento de cada componente:

- **Default:** aparência padrão do componente;
- **Pressed:** resposta visual durante o acionamento;
- **Focused:** campo ativo e pronto para receber entrada;
- **Filled:** campo que já possui conteúdo;
- **Selected:** opção atualmente selecionada;
- **Unselected:** opção disponível, mas não selecionada;
- **Disabled:** componente indisponível para interação.

## Arquitetura

O projeto separa elementos compartilhados, componentes e telas de demonstração:

```text
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
