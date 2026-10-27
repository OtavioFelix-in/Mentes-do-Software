# Mentes do Software — contexto para o Claude

Revista em HTML sobre as escolas de pensamento do design de software (edição 1, outubro de 2026).
No ar em https://otaviofelix-in.github.io/Mentes-do-Software/ (GitHub Pages, branch `main`, raiz).
**Todo push na `main` publica na hora.**

## Regra principal: a revista é do Otávio

A primeira versão foi montada com ajuda do Claude e ainda é só um resumo do que os autores pensam.
O objetivo agora é virar uma revista **dele**, com as opiniões e a voz dele.

- Não escreva reportagem, editorial nem opinião no lugar dele.
- Ajude com perguntas que puxem a opinião dele, com revisão (clareza, português, fatos) e com layout/HTML/CSS.
- Ao revisar um texto dele, mantenha a voz e aponte o que mudar. Não reescreva tudo.
- Fatos sobre autores (datas, citações, obras) devem ser conferidos antes de entrar.

## Estado atual (27/10/2026)

O Otávio vai reler a revista inteira antes de começar a mexer. O próximo passo é ouvir o que ele achou
e o que quer passar. Nada do plano abaixo foi feito ainda.

## Plano de conteúdo (ideias combinadas, a decidir com ele)

1. **Editorial dele na abertura**: por que fez a revista e o que pensa sobre programação. Pode substituir ou vir antes do texto do Naur.
2. **Quadro "Minha leitura" em cada reportagem**: depois do resumo da escola, a opinião dele (concorda, já viu isso no código dele, acha exagero).
3. **Escolher as escolas**: pode cortar as que não dizem nada para ele e incluir outras que ele curte.
4. **Tomar lado no debate** Ousterhout x Martin (reportagem 6), explicando o porquê.

Perguntas para puxar a opinião dele:
- Qual escola mais combina com o jeito que você já programa?
- Qual você acha errada ou superestimada?
- Algum código seu (PI, projetos, trabalho) ficou ruim por um motivo que uma dessas escolas explica?

## Correções técnicas pendentes (achadas na revisão de 27/10/2026)

- [ ] Adicionar `meta description`, `og:title`, `og:description` e `og:image`. Sem eles, o link compartilhado não mostra prévia.
- [ ] Favicon.
- [ ] Tese do Armstrong (`index.html`, reportagem 9): o mirror `mirror.its.dal.ca` não respondeu. Trocar por uma fonte estável.
- [ ] Reportagem 5: o rótulo `O'REILLY` aponta para uma resenha no hamvocke.com. Corrigir o rótulo ou o link.
- [ ] Expediente: crédito do Fred Brooks com escape duplo (`SD&amp;amp;M` aparece como "SD&amp;M").
- [ ] Expediente: a licença da foto do Ousterhout está como "Tcl/Tk". Conferir no Wikimedia.
- [ ] Remover o `<p></p>` vazio no fim de cada bloco "Onde ler".
- [ ] Remover `<meta name="claude:viewport-fit-sides">` (sobra, sem uso fora do Claude).
- [ ] Item `CACM 15(12)` na reportagem 1 está sem link.
- [ ] Links que deram 403 num teste automático: DTIC (Parnas), SE Radio 577 e Microsoft Research (Lamport). Provavelmente é bloqueio a robô. Conferir no navegador.
- [ ] O arquivo EWD do Dijkstra (`cs.utexas.edu/~EWD`) não respondeu no teste. Conferir.

## Estrutura dos arquivos

- `index.html`: a revista inteira, sem build e sem framework.
- `estilo.css`: tokens de cor em `:root`, com modo escuro e estilos de impressão (A4).
- `fotos/XX.jpg`: retratos (Wikimedia Commons, licença livre, créditos no expediente). Cada foto vira uma classe `.ph-XX` no fim do CSS. Quem não tem foto livre aparece com as iniciais (`<span class="pt sem">XX</span>`).

Peças do layout de cada reportagem (`<article class="materia" id="...">`):
`.corrido` (cabeçalho) → `.abre` (número, título, `.linha-fina`) → `.corpo` (`.texto` + `.margem` com a figura SVG) →
`.olho` (citação em destaque) → `.quem` (quem é quem) → `.formulario` / `.folha` ("Onde ler", com visual de formulário contínuo) → `.folio`.
Se entrar uma reportagem nova, adicione também o item no sumário (`nav.sumario`).
