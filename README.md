# Sudoku Java Project

Este projeto é uma implementação do clássico jogo **Sudoku** desenvolvida em Java. A aplicação oferece uma interface gráfica interativa para o usuário jogar, validar e gerenciar partidas de Sudoku.

## 📋 Funcionalidades

- **Tabuleiro Interativo**: Interface visual que permite a inserção de números nas células do Sudoku.
- **Validação de Regras**: O sistema garante que os números inseridos respeitem as regras do Sudoku (linhas, colunas e quadrantes).
- **Controle de Jogo**:
  - Verificação de status do jogo.
  - Funcionalidade para reiniciar a partida.
  - Finalização do jogo.
- **Notificações**: Sistema de eventos para atualizar a interface com base nas mudanças do estado do jogo.

## 🏗️ Arquitetura

O projeto segue uma arquitetura em camadas, promovendo a separação de responsabilidades e organização do código:

- **Model (`br.com.dio.model`)**: Contém as entidades que representam o estado e os dados do jogo, como `Board` (Tabuleiro), `Space` (Espaço/Célula) e `GameStatusEnum`.
- **Service (`br.com.dio.service`)**: Camada responsável pela lógica de negócio. Inclui o `BoardService` para manipulação do tabuleiro e o `NotifierService` para gerenciar eventos e notificações.
- **UI (`br.com.dio.ui`)**: Camada de apresentação responsável pela interface gráfica.
  - **Custom Components**: Componentes personalizados como botões (`ResetButton`, `CheckGameStatusButton`), campos de texto restritos (`NumberText`) e painéis (`SudokuSector`).
  - **Screens/Frames**: Estrutura das janelas e telas principais (`MainFrame`, `MainScreen`).

## 🎨 Biblioteca Gráfica

A interface gráfica do usuário (GUI) foi construída utilizando **Java Swing**.
- O uso de componentes como `JFrame` e `JPanel` permite a criação de uma janela desktop nativa.
- Classes personalizadas estendem componentes do Swing para criar elementos específicos do jogo, garantindo uma experiência de usuário fluida.

## 🚀 Como Executar

Para executar a aplicação com a interface gráfica, utilize a classe `br.com.dio.UIMain`.

```bash
# Exemplo de comando para execução (dependendo de como o projeto for compilado)
java -cp out/production/sudoku br.com.dio.UIMain
```
