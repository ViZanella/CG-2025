#  Refatoração, UML, Herança e Recursos de Áudio

## Descrição Geral
A partir do projeto existente, que exibe um texto se movimentando pela tela no estilo “DVD” (batendo nas bordas), o código foi refatorado para torná-lo mais
organizado, adicionar novos comportamentos de movimento por meio de herança e subclasses, e incorporar recursos de áudio, como sons e música,bem como diagramas
UML que representem tanto o projeto inicial quanto a versão final.

## Princípios SOLID Aplicados

*S - Single Responsibility Principle (SRP)*

Cada classe tem uma única responsabilidade:

MoveTexto: Responsável por desenhar e atualizar a posição do texto.

MoveTextoQuicar, MoveTextoVertical, MoveTextoHorizontal: Implementam diferentes comportamentos de movimento.

AudioController: Gerencia a execução de músicas e efeitos sonoros.

Game: Gerencia eventos e atualização do jogo.

*O - Open/Closed Principle (OCP)*

O sistema permite a adição de novos tipos de movimento sem modificar a classe base MoveTexto, bastando criar uma nova subclasse.

*L - Liskov Substitution Principle (LSP)*

As subclasses de MoveTexto podem ser utilizadas no lugar da classe base sem impactar o funcionamento do código.

*I - Interface Segregation Principle (ISP)*

Cada classe tem apenas os métodos relevantes ao seu comportamento, evitando interfaces grandes e genéricas.

*D - Dependency Inversion Principle (DIP)*

O AudioController é uma dependência injetada, permitindo a reutilização e facilitando mudanças sem afetar o restante do código.

Melhorias de Clean Code

Eliminação de números mágicos: Constantes foram movidas para config.py.

Padronização de nomes: Variáveis e métodos foram renomeados para maior clareza.

Separação de responsabilidades: O código foi modularizado, facilitando a manutenção e a extensibilidade.


## Diagramas UML projeto inicial

![Captura de tela 2025-03-25 184758](https://github.com/user-attachments/assets/7a434a37-e3d4-4310-a48c-94df221baaae)


## Diagramas UML projeto final

![uml_dvd_game](https://github.com/user-attachments/assets/2a476b49-8f18-4e99-9e42-a1d79df125a3)

A refatoração aplicou SOLID e Clean Code para melhorar a estrutura e legibilidade do código. A modularização tornou o sistema mais escalável, permitindo a
adição de novos comportamentos e melhorias futuras com facilidade.
