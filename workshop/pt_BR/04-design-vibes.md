<!-- l10n-sync: source-file="workshop/04-design-vibes.md" -->
# Parte 4: Tematização orientada pelo design

---

Nesta parte, você vai usar os ciclos de planejamento e implementação do Copilot para projetar uma transformação completa do tema. É um desenvolvimento orientado pelo design: comece com uma visão, itere nos elementos visuais e deixe o Copilot cuidar do trabalho pesado de CSS.

## Tarefa 1: Planeje o tema retrô

<!-- track:vscode:start -->
Mude para o modo **Plan** no GitHub Copilot Chat.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Use `/plan` no GitHub Copilot CLI ou pressione **Shift+Tab** até ativar o modo de planejamento.
<!-- track:cli:end -->

Insira este prompt:

> Quero transformar esta página em uma experiência completa de arcade retrô. Planeje uma reformulação visual que inclua: efeitos de linhas de varredura CRT no fundo, brilho neon no título pulsando como um letreiro luminoso, selo VS animado com mudanças nas cores do gradiente, uma camada de brilho sobre os cartões de resultado dos usuários, animações de entrada flutuante nos campos de entrada, texto de carregamento alternando entre verde e roxo e efeitos de brilho ao passar o cursor sobre os quadrados de contribuições. Mantenha o fundo escuro (`#0a0a1a`) e use verde (`#5fed83`) e roxo (`#8a2be2`) como cores de destaque. Use um tema escuro com a fonte de jogos retrô Press Start 2P do Google Fonts.

O Copilot vai gerar um plano detalhado de implementação com todos os efeitos visuais. **Não aceite imediatamente**: revise o plano e itere:

- Sugira ajustes na duração das animações (por exemplo, *"Deixe o pulso neon mais lento, com cerca de 3 segundos"*).
- Pergunte sobre efeitos específicos (por exemplo, *"Como vai funcionar a camada de brilho nos cartões?"*).
- Peça mudanças na abordagem se algo não parecer adequado.

## Tarefa 2: Implemente o tema

Quando estiver satisfeito com o plano, peça ao Copilot para implementá-lo.

> Implemente o plano de tema de arcade retrô que acabamos de criar.

O Copilot vai adicionar várias animações CSS, pseudoelementos e transições na folha de estilos. Isso pode incluir:

- `@keyframes` para as linhas de varredura, o pulso neon, o brilho e os efeitos de entrada flutuante
- Pseudoelementos (`::before`, `::after`) para efeitos de sobreposição
- Propriedades personalizadas de CSS para as cores do tema
- Transições e estados hover para elementos interativos

<!-- track:cli:start -->
Depois que as alterações forem aplicadas, use `/diff` para revisar os estilos antes de aprová-los.
<!-- track:cli:end -->

## Tarefa 3: Ajuste o visual

> **⚠️ Não está vendo as alterações?** Se o tema ou as animações não aparecerem, pare o servidor de desenvolvimento (`Ctrl+C`), reinicie com `npm run dev` e atualize o navegador com **Ctrl+Shift+R**.

Mantenha a prévia do navegador aberta e itere no design. Experimente prompts como:

> O efeito de linhas de varredura está forte demais; reduza a opacidade para 0.03.

> Adicione uma cintilação elétrica sutil ao texto do título.

> O selo VS deveria pulsar com mais intensidade.

Isso é **desenvolvimento orientado pelo design**: você itera no resultado visual em tempo real. Cada prompt refina a experiência até que o resultado fique adequado. Não se contente com algo "bom o bastante" — ajuste o visual até a página parecer uma máquina de arcade.

## Tarefa 4: Atualize as instruções

Suas instruções devem refletir as principais decisões de design para manter os próximos prompts alinhados.

<!-- track:vscode:start -->
Peça ao Copilot Chat:

> Adicione ao `copilot-instructions.md` uma seção de guia de design que descreva o tema de arcade retrô: cores, fontes e estilo das animações.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Peça ao Copilot CLI:

> Atualize as instruções do repositório com um guia breve de design para o tema de arcade retrô: cores, fontes, estilo das animações e a regra de manter a estética neon em qualquer nova interface.
<!-- track:cli:end -->

Quando a página estiver com a aparência desejada, faça commit das instruções e das alterações de design.

## ✅ Parte 4 concluída

**O que você aprendeu:**

- Usar fluxos de planejamento para criar um **sistema visual antes da implementação**
- **Iterar no resultado visual** com prompts de acompanhamento
- **Atualizar as instruções após decisões importantes** para manter a identidade visual
