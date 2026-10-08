# Regras transferidas e plano de migração entre repositórios

## 1. Qual repo faz o quê

- **Destino histórico do jogo novo:** `vicentexk/Mnemos-2.0`.
- **Possível repo de referência:** `vicentexk/Fumiga-GOAT`, que contém o jogo atual, o código, as regras e ferramentas de build.
- **A confirmar antes de qualquer edição:** se Mnemos é o destino para portar uma base seletiva, ou se o usuário quer transformar FUMIGA diretamente no próprio repo. O usuário levantou essa segunda possibilidade, mas a decisão anterior apontava Mnemos como destino.
- **Não trabalhar nos dois ao mesmo tempo sem plano.** Escolher um único repo de escrita para cada sessão/tarefa. Se houver multi-repo, preferir Mnemos como trabalho e FUMIGA como fonte de leitura, até o usuário confirmar diferente.

A sessão que criou este kit está tecnicamente vinculada a `Fumiga-GOAT` e não pode trocar de repositório/branch. O novo usuário deve conferir as opções na tela ao abrir uma sessão.

## 2. O que se sabe sobre conexão de múltiplos repos

A documentação pública consultada do Arena para Agent Mode descreve conectar o GitHub, **escolher um repo e uma branch** e clonar esse repositório no sandbox. Não encontrei ali confirmação pública de seleção simultânea de dois repos por sessão. Portanto, não prometer que a interface permite multi-repo; verificar o seletor na sessão nova.

- Se aparecer uma opção explícita de adicionar outro repositório, usar `Mnemos-2.0` como destino e anexar `Fumiga-GOAT` como referência, dizendo para não o editar sem autorização.
- Se não aparecer, usar Mnemos como repo de trabalho e anexar o ZIP deste kit; para o agente ler **código** FUMIGA, será necessário iniciar uma sessão nele, ou a interface precisa oferecer uma forma de fornecer o source. Os arquivos de regra/lore incluídos no ZIP dão contexto, mas **não substituem o código**.
- Não adicionar FUMIGA como submódulo ou importar a árvore inteira às cegas. Primeiro decidir o que realmente será portado e onde ficará.

Fonte pública consultada: [Arena — Coding in Agent Mode: From Idea to Shipping with GitHub](https://arena.ai/blog/coding-in-agent-mode) (24 ago. 2026). O texto fala em escolher “a repo and a branch”; não declara explicitamente se anexar dois é impossível — por isso a resposta permanece condicional.

## 3. Como reaproveitar FUMIGA sem perder o objetivo do jogo

O código atual foi desenhado para outro loop (simulação/roguelite de controle indireto); a nova aventura exige controle direto, mapas artesanais, itens, dungeons e companheiro único. A direção recomendada para uma auditoria é separar:

1. **Infraestrutura candidata a reaproveitar:** build/teste Windows e Android, boot/tela-base, controles, áudio, save, canvas/renderização e ferramentas — somente depois de ler e validar.
2. **Gameplay que provavelmente precisará de mudança substancial:** movimento/câmera, colisão, interação, mapas, combate, IA de ajudantes, inventário, progressão e fluxo de campanha.
3. **Conteúdo que não deve ser importado automaticamente:** assets visuais antigos (a identidade agora será totalmente nova), textos não revisados e qualquer asset de terceiro cuja licença não tenha sido verificada.

A licença MIT no cabeçalho de cada repo **não significa automaticamente que todo asset ali dentro tenha a mesma licença**. Conferir avisos/créditos, origem dos arquivos e termos de uso antes de portar recursos. Se código MIT for reaproveitado, preservar avisos de copyright/licença necessários.

## 4. Regras do projeto anterior aplicáveis/adaptadas

As cópias em `referencias_fumiga/` são documentos do FUMIGA, específicos daquele jogo. Para este projeto, adaptar os princípios abaixo sem transportar caminhos, números e arquitetura antigos:

- Ler primeiro as instruções do repo de destino (`AGENTS.md`, README, regras locais e build). Se estiver usando FUMIGA como referência, ler as instruções dele também.
- Para decisões de design com impacto grande, pesquisar referências indie e explicar o que se aproveita; pedir escolha do usuário antes de implementação detalhada. As decisões já aprovadas neste kit não precisam ser perguntadas novamente.
- Criar identidade original e evitar personagens humanoides quando forem formigas/animais. Zelda e TUNIC são referências, não fontes de mapas, personagens, música ou arte a copiar.
- Para assets novos, apresentar opções para escolha; integrar somente a arte aprovada, mostrar o resultado e guardar os originais/atribuições conforme o repositório de destino.
- Pensar simultaneamente em teclado/gamepad de Windows e toque de Android; não deixar ações sem equivalente touch.
- Validar código, assets, saves, builds e regressões. Distinguir explicitamente **proposto**, **implementado** e **testado em build/dispositivo**.
- Manter documentação de produção/decisões do novo jogo, mas não presumir que Mnemos deva receber o `MEGA_ARQUIVO.md` ou os scripts específicos de FUMIGA.

## 5. Sobrescritas explícitas das regras legadas

Estas decisões do usuário para a aventura têm precedência sobre regras antigas do FUMIGA:

1. **Sem preview ao vivo.** A Regra 7 antiga do FUMIGA exigia iniciar preview; para este projeto, não iniciar servidor de preview nem pedir que o usuário teste no browser. Entregar builds instaláveis para teste.
2. **Identidade visual totalmente nova.** Não manter as telas/telas de loading/menus ou sprites anteriores só porque uma proposta antiga dizia para mantê-los; nenhum estilo pixel/8-bit anterior está aprovado.
3. **Escopo de campanha completa.** A direção antiga que delimitava a primeira versão à Planície é substituída pela campanha completa; construir o primeiro degrau como marco, não como jogo final.
4. **Plataformas são Windows + Android por enquanto.** Verificar como cada repo empacota essas versões; não tratar PWA/browser como objetivo de distribuição sem aprovação.
5. **Progressão:** itens ampliam capacidades; apenas corações aumentam atributo máximo. Não trazer a árvore de upgrades/roguelite do FUMIGA para esta campanha.
6. **Ajudantes e dungeons:** um ajudante ativo; cada ajudante recebe conteúdo dedicado; uma principal por degrau e cinco opcionais no total como meta inicial, sujeita a ajuste.

Também não transportar automaticamente regras técnicas antigas de pastas (`game/mobile/`, `tools/`, `MEGA_ARQUIVO.md`), tempos de loading, scripts, saves ou fluxos automáticos de PR/merge. Adaptar apenas depois de inspecionar o repo que será escrito e as instruções vigentes. Não criar PR, fazer merge ou publicar Release sem pedido explícito aplicável.

## 6. Limite do kit

O pacote contém documentação e cópias de contexto, **não** contém o source completo de FUMIGA, builds, assets de produção nem novos assets da aventura. O estado anterior de Mnemos foi verificado somente por API pública e deve ser conferido de novo. Nenhum código do jogo novo foi implementado nesta sessão.
