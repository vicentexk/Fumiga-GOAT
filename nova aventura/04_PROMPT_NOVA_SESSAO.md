# Prompt pronto para a nova sessão do Arena

> Anexe `KIT_NOVA_AVENTURA.zip` e cole o bloco abaixo como primeira mensagem. Se a interface oferecer mais de um repo, conecte `Mnemos-2.0` como destino e `Fumiga-GOAT` como leitura/referência.

```text
Estou continuando o projeto de um jogo de aventura de ação e exploração. Leia todo o arquivo KIT_CONTINUIDADE_MNEMOS_2.zip, especialmente 00_LEIA_ME.md, 01_BRIEF_DO_JOGO.md, 02_PLANO_DE_PRODUCAO.md e 03_REGRAS_E_MIGRACAO.md, antes de propor alterações.

REPOSITÓRIOS
- Repo pretendido para o jogo novo: vicentexk/Mnemos-2.0.
- Repo existente que pode servir de base/referência: vicentexk/Fumiga-GOAT.
- Se a sessão aceitar dois repositórios, use Mnemos-2.0 como destino de escrita e Fumiga-GOAT como referência inicialmente. Não edite Fumiga sem eu confirmar.
- Se só puder conectar um repo, não finja que consegue ler o outro: diga o que está disponível. O kit tem regras/lore de referência, mas não tem o código FUMIGA.
- A possibilidade de transformar FUMIGA diretamente, em vez de portar código para Mnemos, ainda precisa ser confirmada antes de editar. Minha preferência registrada anteriormente era ter o jogo novo em Mnemos; quero também avaliar se dá para reaproveitar a base técnica que já existe.

PRIMEIRO PASSO — SEM MUDAR GAMEPLAY
1. Releia as instruções/regras do repo realmente conectado. Verifique o estado atual do repo; não presuma que Mnemos continua vazio.
2. Se FUMIGA estiver disponível, inspecione sua arquitetura, build Windows/Android, testes, saves, lore e licenças, sem copiar diretórios ou assets às cegas.
3. Compare as opções: (A) aproveitar seletivamente infraestrutura/código de FUMIGA e portar para Mnemos, ou (B) desenvolver diretamente em FUMIGA. Diga o custo, risco e implicação de cada uma.
4. Recomende um destino único de escrita e um primeiro degrau vertical de lore. Mostre os achados e peça minha confirmação do destino antes de alterar código.
5. Não reabra decisões que já estão aprovadas no brief. Pergunte apenas o que for indispensável e que ainda esteja em aberto.

DIREÇÃO APROVADA
- Aventura completa de ação/exploração, com controle direto (não point-and-click), em todos os mapas/degraus da campanha.
- Uma formiga protagonista e a colônia ameaçada pela Névoa (não mudar o nome para “Fumaça”).
- Plataformas iniciais: Windows e Android.
- Identidade visual totalmente nova. Ofereça opções de arte e espere minha escolha antes de integrar sprites/telas; nenhum sprite ou estilo final está aprovado.
- A protagonista começa como formiga básica/generalista e ganha novas possibilidades por itens/descobertas. A única melhoria numérica de atributo é aumentar a vida máxima em corações; não criar árvore de força/dano/velocidade ou níveis de atributos.
- Ajudantes são NPCs recrutáveis, apenas um ativo por vez. Cada ajudante deve ter conteúdo/dungeon específico para sua habilidade/identidade.
- Uma dungeon principal por degrau da lore; cinco dungeons opcionais no total como baseline inicial, a revisar após mapear campanha e ajudantes.
- Combate profundo, mas exploração e história também são pilares; HUD minimalista. Sem roguelite, resets de run, mapas/ondas aleatórias ou drafts obrigatórios.
- Trabalhar um degrau da lore por vez depois de planejar a campanha completa em alto nível.
- Usarei builds baixáveis de Windows e Android para testar e enviar feedback. Não quero preview: não inicie servidor nem peça teste pelo browser. Confirme comigo as builds e relatórios de testes.
- Zelda I, The Minish Cap e TUNIC são referências de estrutura/descoberta, não para copiar mapa, música, personagens, arte ou texto.

REGRAS DE CONTINUIDADE
- As instruções do repo-alvo e o brief atual devem ser lidos juntos. Onde uma regra velha de FUMIGA divergir do brief, o brief/decisão atual vence — especialmente “sem preview” e “identidade visual totalmente nova”.
- Faça um plano para campanha completa, mas não tente produzir todos os mapas/áudios/assets numa única entrega.
- Não declare como implementado o que está só planejado; verifique tudo nas builds dos dois sistemas.
- Não faça commit, push, PR, merge, publicação ou mudança destrutiva de saves/assets sem a autorização aplicável.

Ao terminar a auditoria, entregue: (1) resumo dos repositórios visíveis e instruções lidas; (2) diagnóstico de reaproveitamento e licença; (3) recomendação A/B para destino; (4) mapa alto nível dos degraus e dungeons, sem inventar nomes como aprovados; (5) plano do primeiro marco Windows+Android; (6) decisões realmente pendentes para eu aprovar. Pare antes de editar código até eu confirmar o repo de escrita.
```
