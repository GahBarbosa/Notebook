### O que são Conventional Commits?

**Conventional Commits** é um conjunto de convenções para escrever mensagens de commit de maneira padronizada. Ele define um formato claro para registrar mudanças, ajudando a comunicar o propósito de cada commit no histórico do [[Git]]. No formato básico, as mensagens seguem a estrutura:

```
<tipo>(escopo opcional): <descrição>
```

Onde:
- **Tipo**: Indica o tipo de mudança, como `feat` para novas funcionalidades ou `fix` para correções.
- **Escopo**: Opcionalmente especifica a área ou módulo afetado pela mudança, como `auth` ou `ui`.
- **Descrição**: Resume a alteração em uma linha.

Exemplo:
```
feat(auth): add user login functionality
```

Esse formato foi criado para melhorar a legibilidade e o entendimento das mudanças no código, especialmente útil para automação e geração de changelogs.

---

### Como funcionam os Conventional Commits?

O Conventional Commits atua com base em três componentes principais:
1. **Tipos de commit padronizados**: Cada mensagem de commit começa com um "tipo", facilitando a compreensão do que a mudança representa. Tipos comuns incluem:
   - `feat`: nova funcionalidade
   - `fix`: correção de bugs
   - `docs`: alterações na documentação
   - `style`: mudanças de formatação, sem impacto no código (como espaçamentos)
   - `refactor`: alterações que melhoram o código sem adicionar funcionalidades ou corrigir bugs
   - `test`: adição ou alteração de testes
2. **Escopo opcional**: O escopo permite que você defina onde a mudança foi feita (ex: `feat(auth): ...`).
3. **Descrição clara**: Uma linha de descrição que resume a alteração.

O uso de Conventional Commits facilita a geração de **changelogs automáticos**, pois a padronização das mensagens permite que ferramentas identifiquem as mudanças e criem um log organizado para cada versão.

---

### Prós e Contras de usar Conventional Commits

#### Prós
1. **Consistência**: A padronização torna o histórico de commits mais claro e fácil de entender, especialmente para novos membros da equipe.
2. **Automação facilitada**: Ferramentas de CI/CD podem usar Conventional Commits para gerar changelogs automaticamente, aumentar o versionamento e definir lançamentos.
3. **Facilidade na navegação de histórico**: Ao saber o tipo de cada commit, os desenvolvedores conseguem rapidamente identificar e encontrar mudanças específicas (como `fix` ou `feat`).
4. **Documentação melhorada**: O padrão ajuda a tornar o histórico de commits um tipo de documentação valiosa, detalhando o que foi alterado e por quê.

#### Contras
1. **Curva de aprendizado**: Novos desenvolvedores podem precisar de um tempo para aprender e se adaptar ao formato, especialmente em equipes que não utilizam uma prática rigorosa de commits.
2. **Restrição de formato**: Algumas mudanças não se encaixam perfeitamente em um dos tipos predefinidos, o que pode levar a mensagens confusas ou generalizadas.
3. **Necessidade de revisão constante**: Para garantir a consistência, as equipes precisam revisar constantemente os commits, corrigindo formatações incorretas ou orientando membros novos.
4. **Processo mais rigoroso**: A rigidez do formato pode ser vista como uma desvantagem em projetos menores ou em estágios iniciais, onde um padrão formal pode parecer desnecessário.