# Klavi: validação de telas de consentimento Open Finance

Skill para clientes que integram o Open Finance da Klavi via API e personalizam as próprias telas. Ela orienta a construção e valida as telas prontas contra os requisitos obrigatórios (LGPD e Banco Central), antes do envio para a validação oficial da Klavi.

Exemplo de uso: envie capturas, Figma ou código das telas e peça "valide estas telas com a skill da Klavi".

## Como usar

### Claude Code
```
/plugin marketplace add klavi-br/klavi-validacao-telas
/plugin install klavi-validacao-telas@klavi
```

### Claude.ai (Projetos, Team ou Enterprise)
Baixe a pasta `plugins/klavi-validacao-telas/skills/klavi-validacao-telas/`, compacte em `.zip` e envie em **Configurações → Capacidades → Skills**.

### Outras ferramentas de IA (Cursor, GitHub Copilot, ChatGPT, v0, Lovable...)
Anexe ou referencie o arquivo [`klavi-requisitos-minimos-api.md`](klavi-requisitos-minimos-api.md) no prompt ou nas regras do projeto.

Link estável para uma versão específica (recomendado em produção):
```
https://raw.githubusercontent.com/klavi-br/klavi-validacao-telas/v1.0.0/klavi-requisitos-minimos-api.md
```

## Estrutura
```
.claude-plugin/marketplace.json        catálogo do marketplace
plugins/klavi-validacao-telas/
  .claude-plugin/plugin.json           manifesto do plugin
  skills/klavi-validacao-telas/
    SKILL.md                           a skill (frontmatter + requisitos)
klavi-requisitos-minimos-api.md        mesma regra, sem frontmatter, para qualquer IA
CHANGELOG.md                           histórico de versões
```

## Contribuição (time Klavi)
1. Crie uma branch e abra um Pull Request. Nada vai direto para `main`.
2. Siga o template do PR e a regra de versão do `CHANGELOG.md`.
3. Após o merge, crie a tag e a release: `git tag v1.1.0 && git push --tags`.

## Dúvidas
Contato: equipe de integração Klavi.
