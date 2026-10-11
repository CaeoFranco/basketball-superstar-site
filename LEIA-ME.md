# Site do Basketball Superstar - Basquete

Site público do jogo, publicado pelo GitHub Pages (ADR 0024 do repositório do jogo). Não fica aqui nada do código do jogo.

| Arquivo | Para quê |
|---|---|
| `index.md` | A página inicial, com os links da política e dos termos |
| `politica-de-privacidade.md` · `termos-de-uso.md` | Entram depois do parecer jurídico. São cópias geradas pelo `tools/publicar-site.sh` do repositório do jogo, onde fica o texto-fonte. **Não editar aqui:** editar lá e publicar de novo |
| `config.json` | Os interruptores de emergência que o jogo baixa depois da tela de idade |

## Os interruptores (`config.json`)

| Campo | `true` (padrão) | `false` |
|---|---|---|
| `schema` | Sempre `1`. Outro número faz o jogo ignorar o arquivo | — |
| `ads` | Anúncios normais | Nenhum anúncio: os botões de anúncio ficam indisponíveis |
| `interstitials` | Anúncio entre as fases, pelas regras do jogo | Sem anúncio entre as fases (os que dão recompensa seguem o `ads`) |
| `store` | Loja normal | Sem compra nem restauração; uma compra já paga ainda é entregue |

Para mudar: editar o `config.json` aqui no GitHub e fazer o commit. O GitHub Pages leva alguns minutos para publicar, e cada jogador recebe a mudança na próxima abertura do jogo. Campo que faltar fica `true`; um arquivo com erro de digitação não desliga nada (o jogo segue com a última versão boa). Quando usar: os runbooks do repositório do jogo (`docs/runbooks/`).
