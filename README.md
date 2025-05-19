💡 Resumo do Código: ContadorEnergua
O código apresentado implementa o controle e visualização da energia em um jogo Unity, utilizando as bibliotecas UnityEngine, TMPro e UnityEngine.SceneManagement para manipulação de objetos e exibição de texto na interface gráfica. A classe ContadorEnergua, que herda de MonoBehaviour, possui variáveis públicas para armazenar o valor da energia e referenciar o objeto da interface que exibe esse valor na tela.

No método Start(), executado uma vez no início da execução do script, o código localiza o objeto com a tag "ContadorEnergia" e o armazena na variável contador. Isso garante que o sistema tenha uma referência válida para atualizar o valor da energia durante a execução do jogo, evitando erros de referência nula.

A função AddEnergia() permite aumentar a energia, recebendo um valor como parâmetro. A energia só é incrementada se o valor atual for menor que 10.000.000, evitando que o contador ultrapasse um limite lógico. A verificação garante que a energia não fique excessivamente alta, mantendo um controle adequado dentro do jogo.

A função RemoveEnergia() é utilizada para subtrair um valor específico da energia, também passado como parâmetro. Essa função é útil para aplicar penalidades ou reduzir o valor conforme as ações do jogador, mantendo a flexibilidade para diferentes contextos dentro do jogo.

No método Update(), executado a cada quadro, o código atualiza o valor da energia no objeto de texto da interface usando o componente TMP_Text. A exibição na tela é feita convertendo o valor numérico para uma string e concatenando com a palavra "Energia:". Além disso, se o valor da energia cair abaixo de zero, o código carrega de forma assíncrona a cena de índice 2, que geralmente representa uma tela de Game Over ou uma mensagem de falha, indicando que o jogador ficou sem energia suficiente para continuar.

A estrutura do código é modular e bem organizada, garantindo que as funções de adicionar e remover energia estejam separadas e encapsuladas. Isso permite fácil manutenção e reutilização dos métodos em diferentes contextos do jogo. A estratégia de limitar a energia máxima e verificar a queda abaixo de zero garante que o jogo permaneça equilibrado, evitando tanto valores excessivos quanto a continuidade sem energia.

Essa abordagem promove uma experiência de jogo estável e coerente, mantendo o jogador informado sobre a quantidade de energia disponível por meio da interface gráfica constantemente atualizada. O uso de funções separadas para manipulação da energia facilita a extensão do código, caso novas funcionalidades sejam adicionadas, como bônus de energia ou penalidades variáveis.
