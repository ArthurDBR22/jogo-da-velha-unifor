No primeiro jogo foi utilizado a IA gemini

o prompt enviado foi o seguinte

"gemini, preciso criar um jogo da velha
eu vou te passar todos os requisitos solicitados para você analisar, 
eu preciso que você atenda todos os requisitos"

"CDU fornecido pelo professor"

eu testei o jogo e encontrei 2 bugs principais

"1. na hora de traçar a linha de vitoria, a linha fica fora do jogo da velha

2. quando o jogo está em jogador vs PC, eu não consigo prosseguir o jogo
em determinado momento eu não consigo marcar o X no jogo da velha "

por último pedi pra que a IA ajeitase os confetes

"desse jeito está bom, só há um pequeno detalhe que quero que você ajeite, 
os confetes ainda continuam estranhos, agora tem muito confete, tem como você diminuir um pouco? 
eu queria também que eles fossem um pouco mais laterais, 
ele está muito na centralizado, seria mais interessante se ele se espalhasse mais"

basicamente esse foi o prompt utilizado no primeiro jogo da velha

---

No segundo jogo foi utilizado o claude.ai

o prompt foi esse a seguir: "Faça um Jogo da Velha em ambiente web que atenda os requisitos que lhe fornecerei" porém eu só forneci os criterios de avaliação do professor, entao houve erros no exemplo de protótipo e nos fluxos alternativos

o novo prompt foi o mesmo do anterior, só que foi mandado com todos os requisitos fornecidos

Após o teste, foi encontrado um erro na Melhor de 3, onde os empates não estavam constando no passar das rodadas

O ultimo prompt foi para ela corrigir esse erro

Após o ultimo teste, foi cumprido todos os requisitos

---

No terceiro jogo, novamente, foi utilizado o Gemini. Entretanto, diferente do primeiro jogo, o pedido foi extendido.

O prompt foi esse: "Estou fazendo um trabalho em grupo de Requisitos e Modelagem de Sistemas. O trabalho consiste em um jogo da velha na linguagem JavaScript + CSS + HTML baseado nos requisitos que ele passou no repositório do GitHub dele. Para fazer esse trabalho, a IA é responsável por fazer esse trabalho e eu ver como ela se sairá, além de fazer ajustes se ela fizer algo que não foi pedido ou colocar algo a mais do que foi escrito no repositório. Poderia ler o repositório público e verificar o que se pede, além de fazer o código do trabalho para eu ver se está tudo nos conformes? Lembrando que o que estiver faltando irei pedir para implementar depois no código. Aviso: essa conversa será reutilizada para no arquivo RELATORIO_PROMPTS.md.
Link do repositório: *CDU disponibilizado pelo professor*"

Foi feito o teste do jogo e o jogo mostrou a falta de alguns objetivos presentes no CDU:
1. Falta do modo "Contra a CPU" e do formato MD3(melhor de três)
2. A falta da linha de vitória do jogador e os confetes de comemoração

Depois disso, pedi que a IA ajeitasse alguns fatores presentes nos objetivos
O prompt foi esse: "Até agora, você fez tudo certo para uma aplicação simples, mas falta algumas coisas dos objetivos que não foram colocados nessa aplicação que devem ser feitos por você e ditos por mim. Vamos fazer os objetivos por partes. Por agora, adicione um modo de jogo chamado MD3(popularmente chamado melhor de 3); substitua as cores do bloco do jogador vencedor por uma cor da paleta da UNIFOR e adicione uma linha verde por cima da parte do jogador vencedor da rodada com a cor anterior das caixas, com efeitos visuais; por fim, adicione a partir desse parte os efeitos sonoros de todas as funções do jogo(como cliques e música da vitória), para o jogo não ficar silencioso e monótono." 

Foi feito mais um teste e a aplicação precisava dos últimos fatores restantes da CDU:
1. O modo "Contra a CPU"
2. Os confetes de comemoração do jogador vencedor

Foi feito o último prompt, propondo os detalhes restantes e finais do projeto:
O prompt foi esse: "Agora podemos ver a grande diferença comparada com o primeiro protótipo feito aqui, mas ainda falta alguns objetivos que precisam ser concluídos antes dos detalhes finais. Nessa parte, adicione o modo de jogo que será chamado contra o computador(CPU) e altere os modos de jogo anteriores para "formatos de partida", mantendo a lógica do jogo intacta; adicione um efeito de confetes na vitória do jogador daquela rodada, com a paleta de cores dos desenhos do tabuleiro(azul para o X e vermelho para o O)."

Foi feito o último teste do jogo e ele está pronto no index3.html.

---

## Checklist de Critérios de Aceite (Implementação)

- [x] **CA-01 (Fidelidade Visual):** A aplicação utiliza a paleta de cores institucional da UNIFOR (`#003366`, `#0056b3`, `#d97706` e `#f4f6f9`) e possui o subtítulo "UNIVERSIDADE DE FORTALEZA".
- [x] **CA-02 (Regra de Ocupação):** Não é possível sobrescrever uma célula que já possui o símbolo `'X'` ou `'O'`.
- [x] **CA-03 (Bloqueio pós-Fim de Jogo):** Após uma vitória ou empate, o tabuleiro bloqueia cliques em células vazias até que a próxima rodada ou reinício aconteça.
- [x] **CA-04 (Comportamento do Modo CPU):** Quando o modo "Contra o Computador" está selecionado, o sistema executa automaticamente a jogada do robô na vez do 'O' após uma breve pausa.
- [x] **CA-05 (Regra do Melhor de 3):** No formato MD3, o jogo zera o tabuleiro entre rodadas e só encerra a partida completa se um jogador atingir 2 vitórias ou após o fim da 3ª rodada.
- [x] **CA-06 (Efeitos Visuais de Vitória):** A linha contínua é traçada corretamente exatamente sobre as 3 células vitoriosas e os confetes são disparados na tela.
- [x] **CA-07 (Autonomia de Áudio):** O sistema emite os efeitos sonoros via Web Audio API sem depender de downloads ou arquivos `.mp3` externos.

---

## Checklist de Validação do Artefato (CDU)

### 1. Estrutura Mínima
- [x] Nome do caso de uso iniciado com verbo no infinitivo.
- [x] Objetivo claro, direto e com foco em um objetivo principal.
- [x] Tipo do caso de uso informado.
- [x] Atores primário e secundários identificados corretamente.
- [x] Precondições registradas.
- [x] Fluxo principal completo e coerente com o objetivo.
- [x] Fluxos alternativos e de exceção definidos.
- [x] Pós-condições registradas.
- [x] Requisitos não funcionais específicos do CDU registrados.
- [x] Frequência de utilização estimada.

### 2. Qualidade da Especificação
- [x] Passos escritos com linguagem simples e objetiva.
- [x] Ações descritas com verbos no presente do indicativo.
- [x] Alternância entre ação do ator e ação da solução está clara.
- [x] Não há ambiguidade relevante.
- [x] Regras de negócio e mensagens foram referenciadas quando necessário.

### 3. Consistência e Rastreabilidade
- [x] Pontos de entrada e saída dos fluxos alternativos estão explícitos.
- [x] Fluxos de exceção estão vinculados aos passos corretos da solução.
- [x] Referências internas entre passos estão corretas.
- [x] Interface visual está coerente com o fluxo descrito.
- [x] Referências para visão da demanda, glossário e RNF estão atualizadas.

### 4. Revisão Final
- [x] Não há contradições entre seções do artefato.
- [x] Documento revisado por pares.
- [x] Artefato pronto para uso em desenvolvimento e testes.
