# Kit de continuidade — aventura da Névoa

- **Preparado em:** 2026-10-08
- **Destino pretendido:** `vicentexk/Mnemos-2.0`
- **Uso:** anexar `KIT_NOVA_AVENTURA.zip` à nova sessão do Arena e colar `04_PROMPT_NOVA_SESSAO.md` como primeira mensagem.

## O que há neste kit

- `01_BRIEF_DO_JOGO.md` — visão, decisões confirmadas, limites e questões ainda abertas.
- `02_PLANO_DE_PRODUCAO.md` — recomendação de estrutura das dungeons, produção por degraus e inventário amplo de conteúdo/recursos.
- `03_REGRAS_E_MIGRACAO.md` — como aproveitar as regras do FUMIGA sem importar instruções antigas que conflitam com as decisões atuais.
- `04_PROMPT_NOVA_SESSAO.md` — texto pronto para iniciar a nova sessão.
- `referencias_fumiga/` — cópias de referência do `AGENTS.md`, `REGRAS_DE_TRABALHO.md`, `LORE.md` e da direção anterior. São contexto histórico/técnico, não substituem este kit nem as regras vigentes do repositório-alvo.

## Como usar na nova sessão

1. Conecte `Mnemos-2.0` como **repositório de trabalho** e branch de trabalho da sessão.
2. Se a interface oferecer claramente uma segunda conexão de repositório, adicione `Fumiga-GOAT` como **referência**; peça ao agente para lê-lo sem modificar esse repo. Se não houver essa opção, o kit já contém as regras e a lore principais para consulta, mas **não contém o código-fonte do Fumiga**.
3. Anexe `KIT_NOVA_AVENTURA.zip` e cole o prompt do arquivo `04_PROMPT_NOVA_SESSAO.md`.
4. Peça primeiro uma inspeção dos dois repositórios e uma proposta de migração; não comece a reescrever sistemas ou copiar assets antes de confirmar a arquitetura e o destino.

## Estado verificado antes da transferência

Na inspeção read-only anterior, `Mnemos-2.0` era público, estava em `main` e continha somente `LICENSE` (MIT). O agente da nova sessão deve verificar novamente — esse estado pode ter mudado. Já `Fumiga-GOAT` contém o jogo atual, suas regras, código, assets e empacotamento; a sessão que preparou este kit **não alterou gameplay**.

A intenção registrada anteriormente é guardar o jogo novo em `Mnemos-2.0` e usar FUMIGA como referência/candidato a reaproveitamento. Como agora também foi levantada a possibilidade de “modificar o jogo por cima do que já temos”, a nova sessão deve confirmar antes de escrever código se o plano será:

- **A. Mnemos como destino (recomendado para manter o combinado anterior):** auditar FUMIGA como referência e portar somente a infraestrutura/código realmente aproveitável para Mnemos; ou
- **B. FUMIGA como destino:** transformar o jogo existente diretamente no próprio repositório FUMIGA — isso muda a decisão anterior sobre o destino e deve ser confirmado explicitamente.

Não editar os dois repositórios em paralelo sem um plano claro. A identidade visual será totalmente nova; reaproveitamento de lógica não autoriza reaproveitar arte automaticamente.

## Escopo em uma frase

Aventura de ação e exploração não-point-and-click, protagonizada por uma formiga e pela colônia ameaçada pela **Névoa**, com campanha artesanal completa, progressão por itens, ajudantes individuais e dungeons por degrau da lore, para Windows e Android.
