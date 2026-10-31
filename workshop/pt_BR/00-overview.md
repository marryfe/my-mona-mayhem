<!-- l10n-sync: source-file="workshop/00-overview.md" -->
# 🎮 Mona Mayhem — Workshop de GitHub Copilot

---

> **Duração:** ~1 hora  
> **Nível:** Intermediário  
> **Stack:** Astro / Node.js / TypeScript

Construa um aplicativo retrô de arcade para comparar contribuições do GitHub — **Mona Mayhem** — enquanto aprende todo o espectro de fluxos de trabalho do GitHub Copilot. O workshop oferece **duas trilhas**: uma experiência no VS Code e outra com o GitHub Copilot CLI.

---

## 🎯 Escolha sua trilha

- **Trilha do VS Code** — trabalhe no editor e pratique Chat, Plan Mode, Agent Mode, agentes em segundo plano e o ciclo de revisão integrado.
- **Trilha da CLI** — trabalhe no terminal e pratique `copilot`, contexto com `@file`, `/plan`, edições autônomas, `/fleet`, `/delegate` e `/review`.

Siga a trilha que combina com seu fluxo de trabalho.

---

## 📋 Lista de verificação rápida

Antes de começar, verifique:

- [ ] GitHub Copilot está habilitado para sua conta
- [ ] Node.js instalado
- [ ] Git instalado e configurado
- [ ] Seu navegador e terminal estão prontos

<!-- track:vscode:start -->
- [ ] VS Code **v1.107+** (sem atualizações pendentes)
- [ ] Conectado à extensão do **GitHub Copilot**
- [ ] Painel de Chat aberto e Agent pronto
<!-- track:vscode:end -->

<!-- track:cli:start -->
- [ ] GitHub Copilot CLI instalado e disponível como `copilot`
- [ ] Autenticado no CLI com `/login`
- [ ] Confortável usando comandos slash como `/help`, `/plan` e `/review`
<!-- track:cli:end -->

> 💡 **Dica:** Use o DevContainer para um ambiente pré-configurado se quiser um início rápido no VS Code.

---

## 🧠 O que você vai aprender

| # | Habilidade | Descrição |
|---|------------|-----------|
| 1 | **Engenharia de contexto** | Ensine ao Copilot como é sua base de código com instruções, referências e restrições claras |
| 2 | **Planejar Primeiro** | Projete a arquitetura antes da implementação |
| 3 | **Implementação agêntica** | Deixe o Copilot realizar tarefas de programação em várias etapas sob sua supervisão |
| 4 | **Design Iterativo** | Use o Copilot para transformar visuais e refinar detalhes de interação |
| 5 | **Fluxos de Trabalho Paralelos** | Divida o trabalho entre agentes, sessões ou tarefas delegadas |

<!-- track:vscode:start -->
### Foco em Funcionalidades do VS Code

- **Chat + modo Ask** para exploração
- **Plan Mode** para prompts de arquitetura e design
- **Agent Mode** para implementação em múltiplos arquivos
- **Agentes em segundo plano e na nuvem** para polimento em paralelo
<!-- track:vscode:end -->

<!-- track:cli:start -->
### Foco em Funcionalidades do Copilot CLI

- **Sessões interativas do CLI** com `copilot`
- **`/plan` e Shift+Tab** para planejamento estruturado
- **Edições autônomas** com aprovações inline e `/diff`
- **`/fleet`, `/delegate` e `/review`** para paralelismo e controles de qualidade
<!-- track:cli:end -->

---

## 📚 Etapas do workshop

| Parte | Título | Descrição |
|-------|--------|-----------|
| [**01**](01-setup.md) | Configuração e engenharia de contexto | Crie seu repositório, prepare seu ambiente e forneça o contexto adequado ao Copilot |
| [**02**](02-plan-and-scaffold.md) | Planejar e Estruturar | Projete a API e a arquitetura de páginas antes de implementar |
| [**03**](03-agent-mode.md) | Construir o Jogo | Conecte a página de batalha e os gráficos de contribuições com ajuda agêntica |
| [**04**](04-design-vibes.md) | Design Visual Primeiro | Transforme a estrutura base em uma experiência retro arcade |
| [**05**](05-polish.md) | Polimento e Trabalho Paralelo | Use fluxos de trabalho multi-agente para melhorar UX, resiliência e qualidade |
| [**06**](06-bonus.md) | Bônus e Extensões | Explore funcionalidades abertas, fluxos de trabalho de compartilhamento e experimentos extras |

---

## 💡 Dicas práticas

1. **Mantenha o navegador aberto** — observe as atualizações em tempo real enquanto programa.
2. **Faça commits frequentes** — salve pontos de controle limpos enquanto itera.
3. **Refine o plano antes de implementar** — melhores planos levam a melhores resultados.
4. **Revise as mudanças do Copilot** — use a visualização de diferenças ou as ferramentas de revisão do CLI em vez de aceitar cegamente.

<!-- track:vscode:start -->
5. **Use pontos de controle e Desfazer** no chat se uma iteração sair do caminho.
<!-- track:vscode:end -->

<!-- track:cli:start -->
5. **Use `/session`, `/context` e `/share file`** quando quiser inspecionar ou preservar seu trabalho.
<!-- track:cli:end -->
