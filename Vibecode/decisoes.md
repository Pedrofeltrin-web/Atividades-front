# Decisões de design (IDV)

## Conceito
"Imperfeição bonita": identidade quente, humana e manual.

## Paleta
| Nome | HEX | Uso | Por quê |
|---|---|---|---|
| Terracota | `#B0431F` | botões, destaques, vaso | cor do próprio barro; marca a identidade |
| Creme | `#F5EBDD` | fundo | papel/porcelana, mais quente que branco |
| Tinta | `#2B2A22` | texto, seção escura | quase preto com base oliva, mais suave que `#000` |
| Mostarda | `#E0A526` | acentos, selo, linhas | contraste vivo com a terracota |
| Sálvia | `#8A9A7B` | fundo da ilustração | cor complementar fria, equilibra o calor |
| Areia | `#EADBC6` | cards, blocos | variação do creme para hierarquia |

**Correção feita no processo:** a terracota inicial `#C2512F` dava contraste ~4,0:1 com o creme (abaixo de 4,5:1 para texto normal em botão). Escurecida para `#B0431F` (~4,9:1).

## Tipografia
- Títulos: **Fraunces** (serifa com personalidade, evoca o artesanal; itálico para destacar a promessa)
- Texto: **DM Sans** (limpa, legível, deixa o título brilhar)
- Fallbacks: Georgia / system-ui

## Layout
- Hero em 2 colunas: promessa à esquerda, forma-vaso à direita (arco no topo = "janela de ateliê")
- Ritmo de fundos: creme → tinta → creme → areia → creme, para marcar cada bloco
- Estrutura de conversão: promessa → benefícios → como funciona → prova social → preço + CTA

## Escolhas deliberadas
- Ilustração em SVG com formas simples, em vez de imagem de banco (identidade própria, leve)
- Sem animações pesadas; só hover nos botões
- Mobile: colunas empilham em 780px

## Histórico de mudanças (iterações simuladas, ver 01-prompts.md)
| Iteração | Mudança | Motivo |
|---|---|---|
| 1 | Hero e botões ajustados para 375px | conforto no celular |
| 2 | Menu âncora + FAQ com `<details>` | navegação e redução de objeções, sem JS |
| 3 | Estilos inline dos cards movidos para CSS | manutenção |
| 4 | "Vagas restantes" trocado por texto neutro; reduced-motion | evitar urgência falsa; acessibilidade |
