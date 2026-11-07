<p align="center">
  <a href="https://otaviofelix-in.github.io/Mentes-do-Software/">
    <img src="assets/capa-animada.svg" alt="Mentes do Software: as dez escolas de pensamento do design de software" width="100%">
  </a>
</p>

<p align="center">
  <a href="https://otaviofelix-in.github.io/Mentes-do-Software/"><strong>Ler a revista &rarr;</strong></a>
</p>

# Mentes do Software

Revista em HTML sobre as escolas de pensamento do design de software. A edição 1 (outubro de 2026) reúne dez escolas, quem pensou cada uma, onde elas concordam, onde brigam e onde estudar cada ideia.

**No ar:** https://otaviofelix-in.github.io/Mentes-do-Software/

## As dez escolas

| # | Reportagem | Quem |
|---|---|---|
| 1 | Pensar antes de codar | Dijkstra, Parnas, Hoare, Lamport |
| 2 | Pequeno, simples, combinável | Thompson, Ritchie, Pike, Gabriel |
| 3 | Objetos que conversam | Alan Kay |
| 4 | O estado é o vilão | Hickey, Moseley e Marks, Backus |
| 5 | Design que emerge | Beck, Fowler |
| 6 | Funções pequenas ou módulos profundos? | Ousterhout contra Martin |
| 7 | O hardware existe | Acton, Muratori |
| 8 | O negócio no centro | Eric Evans |
| 9 | Sistemas que não caem | Joe Armstrong |
| 10 | Software é feito por gente | Brooks, Conway, Naur, Gross |

Além delas: uma abertura sobre Peter Naur, a síntese "Onde concordam e onde brigam", a biblioteca "Onde estudar" e um plano de sete semanas de leitura.

## Como é feita

- Uma página só, sem build e sem framework: [`index.html`](index.html) e [`estilo.css`](estilo.css).
- Figuras em SVG, animadas com CSS. A animação só roda enquanto a figura está na tela, e fica desligada para quem pede "reduzir movimento" no sistema.
- Versão para impressão em A4.
- Retratos do Wikimedia Commons, com licença livre e créditos no Expediente da revista, em [`fotos/`](fotos).

## Rodar no computador

Não precisa instalar nada. Basta servir a pasta:

```bash
python -m http.server 8000
```

Depois abra http://localhost:8000.

## Publicação

O site é publicado pelo GitHub Pages, a partir da branch `main`, na raiz do repositório. Todo push na `main` vai ao ar.
