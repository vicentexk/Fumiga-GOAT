# Plano de produção e inventário inicial

Este é um plano de trabalho para o jogo completo, não um compromisso de produzir todos os recursos de uma vez. A proposta é fechar a espinha dorsal da campanha e, então, construir **um degrau da lore por vez** em marcos instaláveis.

## 1. Minha recomendação sobre as dungeons

A proposta do usuário é sólida: **uma dungeon principal por degrau da lore** e **cinco dungeons opcionais como baseline inicial para o jogo completo**. Eu manteria esse número provisório porque dá uma meta concreta sem multiplicar o escopo por cada bioma.

### Estrutura recomendada

- **Uma principal por degrau:** contém uma revelação/virada narrativa, puzzles e encontros feitos à mão, um chefe ou clímax equivalente e uma recompensa importante (normalmente um item que abre novas ações).
- **Cinco opcionais no total (inicialmente):** distribuídas ao longo da campanha, não cinco em cada degrau. Devem aprofundar lore, testar itens/ajudantes, oferecer segredos e/ou recompensar exploração. Podem oferecer corações/fragmentos, pistas, colecionáveis ou itens opcionais, respeitando a regra de que a única evolução de atributo é a vida máxima.
- **Dungeon de cada ajudante:** planejar uma dungeon própria para cada ajudante, como o usuário pediu; não reduzir esse escopo a uma sala ou setor sem aprovação. A matriz deverá dizer se cada dungeon de ajudante é também uma principal da lore, uma das cinco opcionais ou uma dungeon adicional. Se o elenco final tiver mais de cinco ajudantes, cinco vagas opcionais não bastam para que todas as dungeons exclusivas sejam opcionais: a campanha terá de integrá-las a degraus principais ou o usuário terá de aprovar mais conteúdo opcional.
- **Um ajudante ativo por vez:** criar puzzles e encontros que valorizem uma escolha; oferecer um local seguro de troca antes dos trechos em que uma habilidade específica é exigida. Nenhuma habilidade opcional deve tornar uma rota obrigatória impossível.
- **Progressão em camadas:** itens recebidos em dungeons principais alteram travessia, combate ou interação; novas áreas e segredos antigos podem ser revisitados. Não recompensar o jogador com aumento de força/velocidade/dano numérico.

### Matriz a preencher antes de detalhar a campanha

| Degrau | Mapa/área e objetivo | Ajudante apresentado/necessário | Item novo | Dungeon principal + clímax | Segredo/revisita | Estado |
|---|---|---|---|---|---|---|
| 1 | A definir após leitura da lore | A definir | A definir | 1 principal | A definir | Não detalhado |
| 2…N | Um por degrau da lore | A definir | A definir | 1 principal por degrau | A definir | Não detalhado |
| Opcionais | Distribuir pelo jogo | Associar só após definir elenco | Recompensas sem atributos novos (exceto corações) | **5 no total como baseline** | Lore/segredos | Meta de planejamento |

Não preencher nomes nem números da tabela sem consultar a lore e confirmar com o usuário.

## 2. Produção em etapas

### Etapa 0 — Reconhecimento dos repositórios (sem editar gameplay)

1. Ler as instruções (`AGENTS.md`, regras, README) do repo de trabalho e registrar conflitos.
2. Verificar o estado atual de `Mnemos-2.0` e do possível repo de referência `Fumiga-GOAT`.
3. Identificar engine, sistema de build, estrutura de pastas, testes, saves e empacotamento Windows/Android.
4. Auditar que partes de FUMIGA são código reutilizável, conteúdo específico do roguelite, assets próprios e assets de terceiros/licenças distintas.
5. Entregar uma proposta curta: **migrar infraestrutura**, **reaproveitar componentes selecionados** ou **começar limpo**. Não copiar pastas inteiras por conveniência.
6. Confirmar com o usuário qual repo será o único destino de escrita. Default histórico: Mnemos como destino; FUMIGA somente referência.

**Saída:** diagnóstico e plano de migração/aproveitamento aprovado, ainda sem reescrever a gameplay.

### Etapa 1 — Bíblia da campanha e regras centrais

1. Mapear a premissa, os degraus da lore, os mapas e o desfecho em uma página por degrau.
2. Aprovar o elenco de ajudantes, a habilidade clara de cada um e como/onde o jogador pode trocar o ajudante.
3. Definir a lista de itens permanentes, a ordem de obtenção, os usos e quais áreas são reabertas por cada item.
4. Fazer a matriz de dungeons: uma principal por degrau, cinco opcionais no total como baseline, desafios de cada ajudante, itens, chefes e requisitos de acesso.
5. Fechar os princípios de controles, combate, vida/corações, checkpoint e saves.

**Saída:** espinha dorsal completa aprovada; só o primeiro degrau fica detalhado em roteiro e mapa de produção.

### Etapa 2 — Identidade visual e modelo de produção

1. Apresentar opções claramente diferentes de identidade visual para o jogo (e, se necessário, para a protagonista/UI).
2. O usuário escolhe antes da criação de sprites finais.
3. Definir escala de trabalho, paleta, legibilidade mobile, animação, atlas/spritesheet, nomes e importação.
4. Gerar uma prova pequena de protagonista + cenário + UI apenas depois da escolha; mostrar a imagem/arte no contexto antes de integrar.
5. Guardar os originais aprovados e documentar a licença/origem de cada recurso externo.

**Saída:** guia de estilo aprovado, com ativos-piloto aprovados e pipeline repetível.

### Etapa 3 — Base jogável multiplataforma

Implementar o mínimo de sistemas que permitam testar o loop real:

- movimento e colisão da protagonista; câmera e transições;
- interação contextual e leitura de objetos/portas;
- um item com utilidade tanto ambiental quanto de gameplay, sem árvore de atributos;
- combate básico com sinais de ataque e resposta;
- corações/receber dano/recuperação;
- diálogo curto, objetivo visível e salvamento;
- controle direto para Windows e controles touch desde o começo;
- teste local sem servidor de preview exposto; automatização dos testes e geração de build instalável.

**Saída:** protótipo de sistemas que não pretende ser o capítulo completo. Não publicar nem chamar de jogo final.

### Etapa 4 — Primeiro degrau vertical completo

Construir uma fatia com começo, progressão e conclusão, não uma sala demonstrativa:

- introdução narrativa, área explorável e diálogos essenciais;
- aquisição de ao menos um item que mude ações;
- recrutamento/participação de um ajudante, se a lore o colocar aqui;
- dungeon principal deste degrau e clímax/chefe;
- atalhos/segredos, objetivo secundário e conteúdo para revisitar;
- tutorial integrado sem excesso de texto;
- build Windows + Android que o usuário possa baixar e testar.

A antiga sequência de áreas da Planície pode servir apenas como inspiração/candidato após auditoria da lore; não é conteúdo final automaticamente aprovado.

**Critério de aceite:** o usuário consegue instalar, iniciar, compreender os controles, concluir o percurso principal e salvar em ambas as plataformas. Corrigir os problemas enviados antes de começar o próximo degrau.

### Etapa 5 — Próximos degraus (iterativa)

Repetir para cada degrau restante: detalhar mapa/objetivos → criar e aprovar recursos → implementar dungeon principal → testar a build nos dois sistemas → incorporar feedback → avançar.

Manter uma visão global dos itens já obtidos, segredos revisitáveis e arcos dos ajudantes para que a progressão não contradiga passos anteriores.

### Etapa 6 — Conteúdo opcional e acabamento de campanha

Integrar as cinco dungeons opcionais segundo a matriz aprovada; verificar acessibilidade, saves, balanceamento, desempenho Android, instalação/atualização, créditos, licença de áudio/arte e integridade das builds. Conteúdo obrigatório e final da lore não pode depender de dungeon anunciada como opcional.

## 3. Inventário de recursos do jogo completo

Este inventário é amplo de propósito; itens marcados dependem da direção visual e do roteiro aprovados. Não gerar todos de uma vez. Produzir e validar por degrau e por conjunto reutilizável.

### 3.1 Arte e animação

**Protagonista**
- sprites/modelo base e variações de direção;
- idle, movimento, giro, ataque rápido, ataque forte/carregado (se aprovado), esquiva, dano, recuperação, interação, carregar/soltar objetos, usar cada família de itens, vitória/derrota e cutscenes;
- silhueta legível em fundos e tamanhos de tela pequenos;
- versão com itens/equipamentos visíveis apenas se a linguagem visual escolhida pedir.

**Ajudantes e NPCs**
- cada ajudante recrutável: retrato/ícone, movimento/follow, parado, ação própria, reação, dano e falas/gestos;
- NPCs de colônia/acampamentos, personagens de lore e missões;
- reações, sinais de conversa, indicação de recrutamento/troca;
- variedade de fauna/insetos sem humanização involuntária.

**Criaturas e chefes**
- inimigos por mapa/bioma e por dungeon, estados de alerta/ataque/dano/derrota, telegraphs e efeitos;
- chefes com silhuetas, fases/ataques legíveis, reações e transições;
- criaturas passivas/ambientais se o roteiro precisar delas.

**Mundo, dungeons e objetos**
- tilesets/terrenos por mapa, bordas/transições, camadas de profundidade e obstáculos;
- identidade visual própria para cada dungeon, entradas/saídas, portas, chaves, interruptores e salas;
- vegetação, fungos, gotas, sementes, pedras, folhas, detritos e props conforme cada ecossistema;
- objetos carregáveis, plataformas, pontes, teias/túneis/outros mecanismos somente quando associados a itens ou ajudantes aprovados;
- peças de puzzle, mecanismos, perigos, checkpoints, pontos de interesse e atalhos;
- mapas/ícones de mapa, diário, pistas e sinais ambientais.

**Itens e feedback visual**
- sprites de itens e pickups; inventário, atalhos/equipamento e descrição;
- recipientes/fragmentos de coração e efeitos de obtenção/vida baixa;
- efeitos de acerto, defesa, esquiva, poeira/terreno, habilidade de ajudante, puzzle resolvido, porta destrancada, baú/recompensa, telegraph e Névoa;
- FX com duração/contraste adequados para celular e sem obscurecer telegraphs.

**Interface e apresentação**
- HUD minimalista (corações, item/ação, ajudante, avisos indispensáveis);
- menus, opções, controles, pausa, mapa, diário, inventário, conversa, crédito e telas de confirmação;
- retratos/ícones apenas se o estilo não antropomorfizar os insetos;
- títulos, transições e cutscenes originais — a direção antiga de “manter telas FUMIGA” está supersedida pela nova identidade total.

### 3.2 Música

Categorias para orçar/planejar, não uma lista de faixas já encomendada:

- menu/título e tema de abertura;
- prólogo/evento inicial (por exemplo, Noite Branca, **somente se a lore final mantiver esse evento**);
- tema calmo de colônia/acampamento e variações de migração;
- tema de exploração para cada mapa/bioma, com camadas para perigo/descoberta quando fizer sentido;
- tema de cada dungeon principal e variações de sala/puzzle/trecho de tensão;
- temas/variações de dungeons opcionais (podem reutilizar motivos próprios, sem reciclar música protegida);
- encontros e chefes com intensificação/fases;
- item encontrado, segredo, puzzle, recrutamento e revelação narrativa;
- pausa/derrota/retorno, vitória, final e créditos.

A antiga faixa de **25–30 temas/variações** é apenas estimativa exploratória. A quantidade real depende do total de mapas, dungeons e orçamento musical. Usar música original ou licenciada corretamente; nunca imitar/copiar trilhas de Zelda/TUNIC.

### 3.3 Efeitos sonoros e ambiências

- passos/movimento por material; pouso, empurrar/arrastar, carregar/soltar e colisões;
- ataques, acertos, falhas, dano, esquiva, defesa/contra-ataque (se existir), vida crítica e cura;
- itens: pegar, equipar, usar, falhar, recarregar (se aplicável), desbloquear nova possibilidade;
- interação com NPC, fala/texto, recrutamento, troca de ajudante e comandos/contexto;
- portas, fechaduras, chaves, baús, alavancas, interruptores, puzzles, mecanismos e atalhos;
- inimigos: passos, estados de alerta, telegraphs, ataques, impacto, dano/derrota;
- chefes: introdução, ataques, telegraphs, mudança de fase, vulnerabilidade, derrota e saída;
- UI: navegação, seleção, confirmação, erro, pausa, mapa, inventário, registro no diário;
- pickups de coração/fragmento e outros colecionáveis;
- ambiências por mapa e dungeon: vento, folhas, água, solo, fauna/insetos, abrigo/acampamento e ruínas;
- sons e camadas próprias da Névoa, aplicados com parcimônia e sem mascarar informação de combate.

### 3.4 Narrativa, diálogos e textos

- diálogos principais por degrau, eventos de transição e finais;
- conversas opcionais de NPCs, acampamento/colônia e callbacks após avanços;
- introdução, recrutamento, troca e falas dos ajudantes; comentários contextuais sem repetição excessiva;
- tutoriais de movimento, combate, itens, dungeons, corações e controles PC/toque;
- objetivos e diário da protagonista, descrições de itens, pistas ambientais e notas colecionáveis;
- mensagens de puzzle, sinais de caminho, placas/inscrições, pistas de segredo e memória/lore;
- missão principal, desvios e missões secundárias, suas condições e resolução;
- introduções de chefes, telegraphs legíveis (preferir comunicação visual/sonora, não apenas texto) e desfechos;
- textos de menus, acessibilidade, controles, pausa, créditos e avisos legais;
- orçamento de localização, dublagem/voz e número de palavras ainda em aberto. Começar com conteúdo escrito/localizável e IDs estáveis se o motor permitir.

### 3.5 Dados, ferramentas e qualidade

- mapa de campanha e grafo de rotas; mapas/salas testáveis e nomes de checkpoints;
- dados das dungeons, requisitos de itens/ajudantes e verificação de ausência de softlock;
- sistema de inventário, save versionado, migração/respaldo e tratamento de perda de progresso;
- remapeamento/legibilidade de controles, acessibilidade visual/sonora, pause e escalas de interface;
- testes automáticos de mapas/puzzles/progressão, regressões de saves e matriz de builds Windows/Android;
- créditos e licenças de cada recurso de terceiros;
- pipeline reprodutível para montar, identificar e distribuir builds de teste.

## 4. Critérios de teste por marco

- Testes automatizados existentes do repo-alvo e validações de assets passam.
- Build instalável abre e roda em Windows e Android. Antes de escolher a solução de runtime, confirmar se o usuário também exige funcionamento offline/sem browser externo; não presumir que a implementação de FUMIGA será a escolhida.
- Entradas equivalentes estão disponíveis nas duas plataformas; ações touch não cobrem HUD/interações.
- O degrau pode ser concluído sem travamentos, softlocks ou ajuda que o jogador não conseguiu recrutar.
- Saves persistem e não são apagados por uma derrota; especificar e testar checkpoints/recuperação.
- Builds são apresentadas ao usuário para download quando o marco estiver pronto; **não usar preview ao vivo**.
- Registrar o que foi implementado, o que está planejado, testes reais, limitações conhecidas e próximo degrau.
