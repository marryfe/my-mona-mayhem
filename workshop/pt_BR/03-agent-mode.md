<!-- l10n-sync: source-file="workshop/03-agent-mode.md" -->
# Parte 3: Construa o jogo com fluxos de trabalho agênticos

---

Nesta parte, o Copilot passa do planejamento à implementação. Em vez de escrever código linha por linha, descreva o que você quer e deixe o Copilot trabalhar nos arquivos necessários.

## Tarefa 1: Conecte a batalha

<!-- track:vscode:start -->
1. Mude para o modo **Agent** no Copilot Chat.
2. Insira este prompt:
<!-- track:vscode:end -->

<!-- track:cli:start -->
1. Volte ao fluxo de programação padrão do Copilot CLI (ou continue no modo autopilot se quiser que ele prossiga até você pará-lo).
2. Se ajudar, mencione o arquivo da página para fornecer contexto adicional: `@src/pages/index.astro`.
3. Insira este prompt:
<!-- track:cli:end -->

   > Adicione JavaScript do lado do cliente à página de batalha para que:
   > 1. Ao clicar no botão Battle, os dois nomes de usuário sejam obtidos dos campos.
   > 2. Os dois campos sejam validados (e um erro seja exibido se algum estiver vazio).
   > 3. Os dados de contribuições dos dois usuários sejam buscados em paralelo pela nossa API.
   > 4. Os gráficos de contribuições sejam exibidos em grids coloridos: cada dia corresponde a um quadrado colorido da paleta do GitHub.
   > 5. Um selo VS seja exibido entre os usuários.
   > 6. O nome de usuário, o total de contribuições e o intervalo de datas sejam exibidos para cada usuário.
   > 7. Os estados de carregamento e os erros sejam tratados.
   > 8. A ação também seja iniciada ao pressionar Enter nos campos de entrada.
   > 9. Por enquanto, use a interface simples já criada.
   >
   > Use interfaces do TypeScript para a estrutura de dados de contribuições.

<!-- track:vscode:start -->
3. Deixe o Agent Mode implementar as alterações em `index.astro`.
4. Revise as alterações propostas na visualização de diff antes de aceitá-las.
<!-- track:vscode:end -->

<!-- track:cli:start -->
4. Deixe o Copilot CLI implementar as alterações em `src/pages/index.astro`.
5. Inspecione as alterações geradas com `/diff` e aprove-as.
<!-- track:cli:end -->

## Tarefa 2: Teste a batalha

> **⚠️ Não está vendo as alterações?** Se a página de batalha não tiver sido atualizada, pare o servidor de desenvolvimento (`Ctrl+C`), reinicie com `npm run dev` e atualize o navegador.

1. Digite `octocat` e `torvalds` como nomes de usuário e clique em **Battle**.
2. Você deverá ver os dois gráficos de contribuições lado a lado, com grids coloridos.
3. Teste os casos de erro:
   - Deixe um ou ambos os campos vazios e clique em Battle: um erro de validação deverá aparecer.
   - Digite um nome de usuário inválido: o app deverá exibir um erro da API.
4. Pressione **Enter** em qualquer campo: a batalha deverá começar como se você tivesse clicado no botão.

## Tarefa 3: Itere com o Copilot

Se algo não estiver exatamente certo, dê feedback diretamente ao Copilot. Por exemplo:

- *"Os quadrados de contribuições estão grandes demais; deixe-os com 12x12px"*
- *"Adicione uma dica ao passar o cursor que mostre a data e o número de contribuições"*
- *"O estado de carregamento precisa de uma animação pulsante"*

<!-- track:vscode:start -->
O Agent Mode lida naturalmente com alterações em vários arquivos e iterações. Cada prompt de acompanhamento aproveita a conversa anterior, permitindo aprimorar a implementação aos poucos sem recomeçar.
<!-- track:vscode:end -->

<!-- track:cli:start -->
As sessões do Copilot CLI mantêm o histórico, então cada prompt de acompanhamento continua a partir do anterior. Use `/session` ou `/context` para consultar o contexto que o Copilot está mantendo e `/review` após uma iteração maior para procurar erros ou oportunidades de melhoria.
<!-- track:cli:end -->

## Dicas para esta parte

- **Explique com precisão o que você quer**: requisitos claros levam a resultados melhores.
- **Divida tarefas grandes em prompts menores** se o Copilot sair do rumo.
- **Revise as alterações antes de aceitá-las**: é mais rápido inspecionar o código gerado do que reescrevê-lo depois.
- **Teste o app após cada etapa de implementação** para localizar problemas rapidamente.

## ✅ Parte 3 concluída

Você aprendeu a:

- Usar o Copilot para **implementar alterações em vários arquivos**
- **Iterar nos resultados** com feedback específico
- Acompanhar o **ciclo completo de uma funcionalidade**: implementação, revisão, testes e refinamento
