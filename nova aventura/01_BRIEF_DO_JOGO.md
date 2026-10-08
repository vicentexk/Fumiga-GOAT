# Brief do jogo — aventura da Névoa

**Atualizado:** 2026-10-08

**Documento-base para a nova sessão:** este brief consolida as decisões recentes do usuário e substitui as partes incompatíveis da antiga direção da Planície.

## 1. Visão

Criar uma aventura completa de ação, exploração e narrativa, com uma **formiga protagonista** atravessando todos os mapas/degraus da campanha enquanto ajuda a colônia ameaçada pela **Névoa**. A câmera e a progressão acompanham a protagonista. A experiência deve equilibrar combate elaborado com exploração, segredos, dungeons, personagens e diálogos.

- **Não é point-and-click:** o jogador controla a protagonista diretamente, com comandos responsivos.
- **Campanha artesanal e persistente:** sem roguelite, runs que apagam progresso, geração procedural obrigatória, ondas aleatórias ou drafts de poderes.
- **Plataformas iniciais:** Windows e Android.
- **Identidade visual:** inteiramente nova. Não manter por obrigação a identidade/telas de FUMIGA, nem assumir que o estilo 8-bit mencionado em uma proposta antiga continua valendo.
- **Título e nome da protagonista:** não decididos.

## 2. Decisões confirmadas pelo usuário

| Tema | Decisão atual |
|---|---|
| Premissa | Uma formiga protagonista e a colônia sob ameaça da **Névoa**. Não renomear para “Fumaça”. |
| Gênero | Aventura de ação, exploração e história, com controle direto; não point-and-click. |
| Inspirações | *The Legend of Zelda* (especialmente o primeiro jogo e *The Minish Cap*) para itens, exploração e dungeons; *TUNIC* como referência para segredos e pistas. Inspirar sem copiar conteúdo protegido. |
| Escopo | Jogo completo em todos os mapas/degraus da lore. A antiga proposta de fazer somente a Planície está supersedida; a Planície pode ser o primeiro marco, não o limite do jogo. |
| Plataformas | Windows e Android por enquanto. O formato de pacote e versões mínimas ainda precisam ser inspecionados/definidos. |
| Arte | Identidade visual totalmente nova. Nenhum estilo, sprite, personagem ou arte final foi aprovado. |
| Protagonista | Começa como formiga básica/generalista e aprende novas possibilidades gradualmente, sobretudo através de itens e habilidades de uso. Espécie e visual exatos continuam em aberto. |
| Progressão numérica | A única estatística máxima que pode aumentar é a **vida máxima em corações**. Sem árvores de força, velocidade, dano ou níveis de atributos. Itens podem ampliar ações e possibilidades sem virar aumentos numéricos de atributos. |
| Ajudantes | São personagens/NPCs recrutáveis; somente **um ajudante ativo** acompanha a protagonista por vez. |
| Dungeon de cada ajudante | Planejar **uma dungeon própria e específica para cada ajudante**, concebida em torno da habilidade/identidade dele. Ainda falta decidir se cada uma conta como principal da lore, como uma das cinco opcionais ou se exige vagas adicionais; não reduzir a requisito de uma sala/seção sem consultar o usuário. |
| Dungeons principais | Uma dungeon principal por degrau da lore. Portanto, o total só pode ser fixado depois de mapear os degraus da campanha. |
| Dungeons opcionais | Planejar **cinco no total para começar** como alvo inicial de escopo, não cinco por bioma/degrau. Revisar quando a quantidade de ajudantes e a lore estiverem mapeadas. |
| Teste do usuário | O usuário quer baixar builds instaláveis de Windows e Android e testar; **não quer preview**. Não iniciar servidor de preview para este projeto. |
| Produção | O escopo é grande; desenvolver e validar um degrau da lore por vez, após planejar a espinha dorsal da campanha completa. |

## 3. Princípios de design recomendados

Estes pontos desenvolvem as escolhas do usuário; a nova sessão deve validar detalhes antes de os transformar em sistemas definitivos.

1. **Item novo = nova possibilidade.** Um item deve habilitar uma ação legível (atravessar, alcançar, revelar, manipular, lutar de outra forma), não apenas aumentar um número de dano.
2. **Corações como única progressão de atributo.** Aumentos de vida máxima podem vir de recompensas de exploração/dungeons; outros atributos não sobem por nível ou grind. A quantidade e o ritmo dos corações são decisões de balanceamento abertas.
3. **Um ajudante ativo, sem microgerenciar um esquadrão.** Fazer troca em locais seguros (por exemplo, acampamentos) é uma solução a avaliar para permitir escolher o ajudante adequado sem trocar no meio de toda sala.
4. **Dungeons específicas sem softlock.** Se uma dungeon exigir um ajudante, o jogador precisa saber isso antes de entrar e ter acesso ao ajudante necessário; prever saída/retorno ou troca segura. Não bloquear a campanha por um recrutamento opcional perdido.
5. **Exploração com rota principal clara e desvios.** Segredos e pistas devem ensinar o mundo sem depender de excesso de HUD ou de copiar o manual de *TUNIC*.
6. **Combate complexo pela leitura e uso do espaço.** Padrões, posicionamento, timing, terreno, objetos e habilidades conquistadas dão profundidade; não usar hordas aleatórias como estrutura de campanha.
7. **Personagens não humanoides.** A protagonista, ajudantes, inimigos e chefes devem preservar uma leitura de fauna/insetos e não de humanos fantasiados.
8. **Mobile tratado desde o design.** Cada ação de teclado/gamepad precisa ter equivalente de toque confortável, botões dimensionados e HUD legível; não deixar o Android como conversão tardia.
9. **HUD minimalista.** Mostrar o essencial (corações, item/ação atual e ajudante) e deixar mapa, inventário completo, diário e diálogos em interfaces próprias ou sob demanda.

## 4. Estrutura narrativa e mapas

A proposta antiga mencionava os seis mapas/biomas de FUMIGA como possível espinha dorsal e a Planície como começo. Isso **não fecha a lista final de mapas**. Se FUMIGA estiver disponível como repo de referência:

- ler a lore e mapear todos os degraus, biomas e eventos existentes;
- propor quais elementos podem ser preservados, reinterpretados ou descartados;
- preservar o nome **Névoa** e a premissa central;
- apresentar a espinha dorsal da campanha inteira para aprovação, sem reescrever a lore canônica de imediato;
- detalhar e implementar apenas o primeiro degrau depois da aprovação.

A narrativa pode ser nova e acompanhada pela protagonista. Rainha, colônia, acampamentos e ajudantes podem ser NPCs importantes; confirmar a continuidade de personagens e eventos ao auditar a lore. Não declarar nomes de biomas, chefe, inimigos ou missões como aprovados só porque aparecem na direção antiga.

## 5. Inspirações e limites de originalidade

- **Zelda I / *The Minish Cap*:** referência para exploração, aquisição de itens que mudam o que o jogador consegue fazer, dungeons, puzzles e chefes. Criar mapas, itens, músicas, personagens, diálogos e arte próprios.
- **TUNIC:** referência para descoberta, pistas ambientais e segredos que recompensam observação. Não copiar páginas, mapas, símbolos, estilo de arte ou soluções específicas.
- O novo mundo, a identidade visual e o elenco devem ser originais. Referências orientam sensações/estruturas, não substituem design próprio.

Fontes consultadas anteriormente:
- [The Legend of Zelda — Nintendo](https://www.nintendo.com/en-gb/Games/NES/The-Legend-of-Zelda-796345.html)
- [The Legend of Zelda: The Minish Cap — Nintendo](https://www.nintendo.com/games/detail/Uq4mHxYWIHPUlTlOd967IkJ1lvpCuYak)
- [TUNIC — Finji](https://finji.itch.io/tunic)

## 6. Pontos ainda em aberto (não inventar como fatos)

### Direção/escopo
- Nome final do jogo, protagonista e elenco; se o título FUMIGA será mantido ou se o projeto terá outro título.
- Se Mnemos receberá uma migração seletiva do código FUMIGA, ou se a implementação começará limpa. Não há código no estado de Mnemos verificado anteriormente.
- Quantos degraus da lore e mapas entram na campanha final; se os seis mapas de FUMIGA serão mantidos.
- Quantos ajudantes existirão; quais são suas espécies, personalidades, habilidades e ordem de recrutamento.
- Se os cinco opcionais são o total inicial de dungeons opcionais do jogo completo ou um primeiro lote de planejamento (a recomendação deste kit é **cinco no total como baseline**, sujeito a revisão).
- Se cada ajudante terá uma dungeon completa própria ou uma seção/desafio exclusivo integrado a uma dungeon maior.

### Gameplay
- Itens permanentes, inventário/equipamento, ações de combate, interação e regras para carregar objetos.
- Número e ritmo de corações, fragmentos/recipientes de coração e recuperação de vida.
- Troca de ajudante, checkpoints, derrota/respawn, saves e viagens entre áreas.
- Visão/câmera, tamanho das áreas, densidade de segredos, dificuldade e acessibilidade.

### Arte, áudio e distribuição
- Estilo visual, paleta, resolução, proporções dos sprites, animação, interface e orientação Android. **Oferecer opções visuais e obter escolha antes de integrar arte.**
- Teclado, gamepad e controles touch exatos; recomenda-se prototipar layout mobile antes de produção extensa.
- Português apenas ou localização; diálogos somente em texto ou com voz.
- Faixas de áudio e orçamento final; a estimativa antiga de 25–30 temas/variações era preliminar, não uma quantidade aprovada.
- Formato do instalador Windows, APK/ABIs Android, requisitos mínimos, operação offline e assinatura/distribuição. Inspecionar o código e as pipelines antes de prometer pacotes.

## 7. Regra de escopo desta transferência

Uma direção completa não significa produzir o conteúdo inteiro numa entrega. Planejar a campanha inteira em alto nível, mas implementar em unidades de teste: **um degrau da lore por vez**, com build instalável do marco. Não encerrar o jogo na Planície nem tentar produzir todas as dungeons, diálogos e artes de uma só vez.
