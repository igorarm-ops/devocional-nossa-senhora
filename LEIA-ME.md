# Sob o Manto de Maria — Devocional da Esposa

> *Dedicado a Nossa Senhora, modelo e Mãe das esposas.*

App diário para a esposa crescer em santidade e amar o marido **à escola de Maria**.
**Uma reflexão diferente para cada dia do ano** (366 dias), a partir de **Nossa Senhora**,
das **cartas dos papas**, dos **santos** e da **Palavra de Deus**. Cada dia traz:
ensinamento (com a fonte), reflexão curta, **reflexão profunda**, **♥ gesto de amor do dia**,
**✦ oração** e versículo.

Identidade mariana: **azul** (o manto), **ouro** (a graça), **rosa** (o amor) e a **coroa de
doze estrelas** (Ap 12,1) no ícone. O marcador `{ESPOSO}` é trocado pelo nome dele.

## Link / instalar
- **App publicado:** https://igorarm-ops.github.io/devocional-nossa-senhora/
- **iPhone:** abra no Safari → Compartilhar (↑) → Adicionar à Tela de Início.
- **Android:** abra no Chrome → menu ⋮ → Instalar app.
- Funciona offline depois da primeira abertura.

## Notificação diária
Push diário às **9h (horário de Brasília)** com o tema e um trecho da reflexão, enviado por um
robô automático no **GitHub Actions** (não depende de ninguém ligado). Para ativar: abrir o app
instalado → **🔔 Lembrete diário** → Permitir → enviar o código gerado para cadastro.

## Estrutura / regenerar
- Acervo: 46 ensinamentos marianos vetados (`dados/ensinamentos.json`).
- 366 reflexões (`dados/reflexoes/` → `reflexoes-ano.js`).
- Build em `dados/`: `python gerar_briefs.py` → reflexões → `python mesclar_validar.py`.
  Auditoria: `python verificar_app.py`. Ícone: `python gerar_icone.py`.
- Ao mudar conteúdo: `git commit` + `git push` (Pages republica) e subir a versão do cache em `sw.js`.

## Arquivos do app
`index.html, styles.css, app.js, ensinamentos.js, reflexoes-ano.js, bilhetes.js,
manifest.webmanifest, sw.js, icone.svg, icone-192.png, icone-512.png, apple-touch-icon.png`
+ `push/` (robô) + `.github/workflows/lembrete.yml` + `dados/` (fonte e scripts).

*“Eis aqui a serva do Senhor; faça-se em mim segundo a tua palavra.” (Lc 1,38)*
