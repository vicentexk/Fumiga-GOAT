# FUMIGA — Direção da nova aventura

**Data:** 2026-10-08
**Branch:** `arena/ad8884de-fumiga-goat`
**Status:** direção conceitual aprovada como base; **documentação apenas** nesta entrega. A gameplay atual não foi alterada.

> Este documento registra as escolhas do usuário para uma possível mudança de gênero. Não declara que a aventura já está implementada nem substitui a lore canônica atual. A produção de código e a reescrita integral da lore ainda precisam de detalhamento e autorização próprios.

## 1. Visão

Transformar FUMIGA de um roguelite de comando de colônia em uma **aventura de ação e exploração, top-down e centrada em história**, acompanhando uma formiga protagonista durante a subida da colônia para escapar da Névoa — percebida visualmente como fumaça.

A experiência deve combinar **combate complexo com bastante exploração**, sem voltar a ondas intermináveis. Os seis biomas existentes podem ser reinterpretados como capítulos exploráveis, com espaços feitos à mão, objetivos, desvios, atalhos e encontros planejados.

### Princípios de design

1. A câmera, a história e a progressão acompanham sempre a protagonista.
2. A protagonista é uma formiga não humanoide que pode carregar objetos, atacar e desenvolver capacidades gradualmente.
3. As demais formigas são NPCs; algumas podem ser recrutadas como ajudantes.
4. Combate e exploração são pilares simultâneos. A complexidade vem de leitura de padrões, posicionamento, terreno, objetos e apoio dos ajudantes — não de hordas aleatórias.
5. A campanha é persistente: sem reinício roguelite, mapas aleatórios ou drafts obrigatórios.
6. O HUD de gameplay fica minimalista; título, telas de carregamento, menus, árvore, cutscenes e demais telas conservam sua identidade visual atual.
7. Os sprites de gameplay recebem um estilo 8-bit mais simples; os fundos de bioma permanecem detalhados como interpretação inicial do pedido “um pouco de cada”.

## 2. História e cânone

- **Premissa a preservar:** a colônia está subindo para fugir da ameaça que avança.
- **Ponto de vista novo:** a jornada passa a ser narrada pela experiência da protagonista — o que ela vê, transporta, aprende, recorda e faz pelos demais.
- **Rainha e colônia:** deixam de ser controladas diretamente durante a expedição e passam a ser personagens/NPCs importantes, incluindo os acampamentos e a caravana em movimento.
- **A ameaça:** a decisão atual é manter a **Névoa** canônica, com aparência de fumaça; não renomear o fenômeno nesta etapa.
- A Noite Branca, os seis biomas e a Pálida podem continuar servindo de espinha dorsal, mas a relação dos eventos com a protagonista deverá ser revista e aprovada antes de substituir `LORE.md`.

## 3. Protagonista e progressão

A escolha atual é começar com uma **formiga generalista básica**, ainda sem espécie real específica definida. A personagem começa com ações simples — movimentar-se, carregar objetos leves e atacar — e pode ganhar capacidades permanentes enquanto a campanha avança.

**Direção proposta, ainda não detalhada:** novas capacidades são aprendidas em momentos da história, por exploração, encontros e relação com os NPCs. A evolução não usa ofertas aleatórias por run. Como o projeto exige personagens baseados em fauna e insetos reais, a espécie/forma visual da protagonista será definida antes da criação de sprites finais.

A forma exata de “mudar aos poucos” ainda precisa ser decidida: pode significar aprender habilidades, melhorar atributos, alterar a aparência ou uma combinação. Nenhuma mudança de espécie ou metamorfose está aprovada por este documento.

## 4. Ajudantes recrutáveis

- Os ajudantes são NPCs recrutados durante a jornada; não são um exército selecionado por cartões.
- **Decisão confirmada:** somente **um ajudante ativo** acompanha a protagonista por vez.
- Direção proposta: o ajudante acompanha por IA simples e oferece uma capacidade clara de exploração ou combate, sem exigir microgerenciamento.
- Exemplos candidatos, não escolhas finais: Tecelã para criar travessias de seda; Matabele para socorro; Cortadeira para interagir com folhas e obstáculos; Prata para farejar trilhas.
- A primeira ajudante candidata para a Planície é uma **Tecelã**, pois demonstra a combinação entre recrutamento e travessia. Ainda precisa de aprovação antes de virar conteúdo do jogo.

## 5. Ciclo de gameplay

1. Sair de um acampamento da colônia com uma pista ou objetivo.
2. Explorar a área e observar sinais, rastros e memórias de feromônio.
3. Carregar, soltar ou usar um objeto para resolver um obstáculo, fazer uma entrega ou acessar um desvio.
4. Lutar, evitar o encontro ou usar o ambiente a favor da protagonista.
5. Ajudar/recrutar uma formiga, abrir um atalho e avançar a migração.
6. Salvar o progresso e continuar a subida; uma derrota não apaga a campanha nem elimina permanentemente o recrutamento.

A última regra de recuperação é uma recomendação de design e precisa de detalhamento antes da implementação.

## 6. Combate

O usuário pediu combate complexo, em equilíbrio com bastante exploração. A proposta é que a personagem tenha poucos comandos básicos, com profundidade pela combinação e pelo timing:

- ataque rápido de mandíbulas;
- ataque mais forte/carregado para interromper ou quebrar defesas;
- esquiva e reposicionamento;
- habilidades permanentes aprendidas durante a história;
- apoio contextual do ajudante ativo;
- ataques dos inimigos com sinais claros, padrões diferentes e interação com terreno/objetos.

Chefes são confrontos planejados de capítulo, não parte de uma sequência aleatória de ondas. A protagonista continua sendo uma formiga: não usar armas ou postura humanoides.

**A definir:** comandos exatos, defesa/bloqueio ou contra-ataque, recursos de combate, frequência dos encontros e profundidade das melhorias.

## 7. Exploração e campanha

Direção proposta: seis capítulos/biomas feitos à mão, conectados por trilhas, acampamentos e atalhos. Cada região deve oferecer uma meta principal legível, rotas opcionais, segredos e oportunidades de ajudar/recrutar NPCs. Os eventos devem apoiar a fuga ascendente da colônia e revelar a lore pela experiência da protagonista.

O formato preciso de mundo semiaberto, a navegação, o tamanho dos capítulos e a estrutura das missões permanecem decisões de produção. O mundo procedural atual não deve ser presumido como o formato final da aventura.

## 8. Primeiro capítulo: Planície do Amanhecer

**Escopo aprovado para a primeira entrega de gameplay:** um capítulo completo da Planície, com várias áreas, desvios, ajudantes e chefe — e não apenas uma sala demonstrativa. Trata-se de uma conversão significativa; o capítulo deve ser produzido em marcos testáveis.

Sequência de referência, ainda ajustável:

1. **Acampamento da migração:** apresentar a protagonista, a rainha/NPCs e a necessidade de encontrar uma rota segura.
2. **Campo de Orvalho:** ensinar movimento, interação e transporte de um objeto relevante.
3. **Raízes da Planície:** apresentar um desafio ambiental com caminho principal e desvio opcional, incluindo rastros/memória.
4. **Recrutamento:** ajudar uma formiga e mostrar a utilidade de um único ajudante ativo; a Tecelã é a candidata inicial, ainda não aprovada como conteúdo final.
5. **Trilha do Tambor:** combate planejado, uso de terreno e um atalho.
6. **Tamborilador:** confronto de chefe com avisos legíveis de impacto e janelas de contra-ataque; sem ondas aleatórias.
7. **Conclusão:** a protagonista ajuda a caravana a alcançar o próximo trecho da subida, abrindo a Floresta como continuação da jornada.

Os nomes das áreas, o roteiro completo, tarefas secundárias, espécies dos inimigos, recompensas e detalhes do chefe ainda não estão fechados.

## 9. HUD e controles

**Decisão visual:** HUD minimalista. Proposta inicial: indicadores pequenos para vida, objeto carregado e ação/habilidade do ajudante; mapa, diário e objetivos detalhados ficam em tela própria ou sob demanda. Não manter na gameplay os painéis de população, comida, ondas, essência e seleção de exército se não servirem à aventura.

Os comandos ainda serão definidos. A experiência precisa funcionar com teclado/mouse e com toque, sem duplicar gameplay na pasta mobile: toda ação nova terá equivalente de toque, controles legíveis e hitboxes adequadas.

## 10. Direção de arte

- Gameplay: sprites mais simples, com leitura **8-bit retrô** para protagonista, ajudantes, criaturas, itens/objetos interativos e efeitos.
- Fundos e cenário dos biomas: manter a arte detalhada atual nesta proposta, conciliando o contraste de estilos com paleta e silhuetas legíveis.
- Fora da gameplay: manter os visuais atuais de título, carregamento, menus, árvore, cutscenes e demais telas.
- O tamanho de sprite, resolução de trabalho, número de cores e método de animação ainda serão definidos em uma etapa visual. Nenhum sprite novo foi criado nesta entrega.
- Qualquer arte nova deverá seguir as regras do projeto: opções para escolha, exibição da arte aprovada e preservação do original/espelho antes de integração.

## 11. Referências pesquisadas

- **TUNIC** — a descrição oficial destaca mundo interligado, páginas de manual, pistas e segredos. Adaptação possível: diário da protagonista, trilhas de feromônio e descobertas que ensinam o mundo sem excesso de HUD. [Página oficial da Finji](https://finji.co/games/tunic/).
- **A Short Hike** — a página oficial incentiva tanto seguir trilhas quanto explorar desvios e encontrar tesouros. Adaptação possível: desvios opcionais e descobertas tranquilas entre os momentos de combate. [Página oficial](https://ashorthike.com/).
- **Hyper Light Drifter** — a página do jogo descreve exploração de um mundo arruinado, conhecimento perdido, caminhos ramificados e segredos. Adaptação possível: história contada pelo ambiente e rotas alternativas; não tomar como modelo a dificuldade ou a intensidade de combate. [Steam](https://store.steampowered.com/app/257850/Hyper_Light_Drifter/).

As referências são inspirações de estrutura e sensação; a identidade, lore e arte do FUMIGA devem permanecer próprias.

## 12. Impacto técnico e salvaguardas

A versão atual é um roguelite de comando indireto de unidades. Uma aventura de controle direto exige redesenhar o ciclo de gameplay — movimento da protagonista, câmera, interação, inventário/carga, combate, recrutamento, mapas, HUD, checkpoints e progressão. Sistemas existentes podem ser aproveitados seletivamente, mas não se deve presumir que a simulação atual simplesmente se converte em Zelda-like.

A migração também precisa decidir o que acontece com os saves atuais. A recomendação é não sobrescrever progresso antigo sem uma estratégia aprovada de compatibilidade.

Antes de implementar:

1. Fechar a proposta detalhada de controles, combate, carga, recrutamento e história da Planície.
2. Criar e exibir opções visuais para os sprites de gameplay; integrar apenas a escolha aprovada.
3. Confirmar compatibilidade de teclado/toque e o plano de saves.
4. Implementar por marcos e validar a experiência no preview, com testes headless e de navegador.
5. Atualizar o `MEGA_ARQUIVO.md` na entrega de cada implementação; sincronizar os documentos incorporados se algum dos seis originais for editado.

## 13. Estado e validação desta entrega

- Direção de aventura, foco narrativo na protagonista, ajudantes, Névoa, HUD minimalista, sprites 8-bit e capítulo completo da Planície: **aprovados como base conceitual pelo usuário**.
- Documento formal criado a pedido do usuário.
- Código, assets, saves e gameplay: **não alterados**.
- `LORE.md`: **não reescrito**; este documento registra a direção, não substitui o cânone em vigor.
- `node game/test/docs.mjs`: passou; seis originais incorporados no MEGA íntegros, 113.359 bytes e hashes preservados.
- `npm run test:quick`: **29/29** testes passaram.
- `npm run inspect`: Chromium PC + mobile, telas e seis mapas; sem erros JS, 404 ou glifos ausentes; RUN a 60 FPS nos seis mapas.
- Preview `http://127.0.0.1:8000/game/`: HTTP 200; capturas PC/mobile do título e da gameplay atual inspecionadas. Nenhuma gameplay foi alterada.
- Próximo passo: revisar e detalhar a Planície e as capacidades progressivas da protagonista; obter aprovação da arte antes de sua integração e autorização explícita antes de começar a mudança de gameplay.
