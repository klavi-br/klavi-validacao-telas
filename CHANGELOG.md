# Changelog

Todas as mudanças relevantes desta skill. Formato baseado em [Keep a Changelog](https://keepachangelog.com/pt-BR/1.1.0/) e [SemVer](https://semver.org/lang/pt-BR/).

Regra de versão:
- **MAJOR** (2.0.0): muda texto marcado como COPIAR EXATAMENTE, adiciona ou remove um requisito OBRIGATÓRIO. Clientes precisam revisar telas já construídas.
- **MINOR** (1.1.0): novo item OPCIONAL/RECOMENDADO, esclarecimento que não muda o que é exigido.
- **PATCH** (1.0.1): correção de digitação fora dos textos legais, formatação.

## [2.0.0] - 2026-11-18
### Adicionado
- Parâmetro `tipo_jornada` (`completa` | `reduzida`). Padrão: `completa`. Na validação, se não for informado, a IA infere o tipo pela primeira tela enviada e informa qual jornada considerou.
- Tabela comparativa das duas jornadas no início do documento.
- Jornada reduzida (seção 5.5): tela inicial que combina a primeira tela e a Confirmação dos Dados, sem conteúdo específico da instituição, e vai direto da Seleção de Instituição para o Redirecionamento.
- Novos requisitos obrigatórios `REQ-RDZ-01` a `REQ-RDZ-03`, incluindo o Disclaimer único (COPIAR EXATAMENTE), que substitui os Disclaimers #1, #2 e #3 na jornada reduzida.
- Parâmetro `exibir_cpf_contato` (padrão `true`) para a jornada reduzida. Com `false`, os campos de CPF e contato não aparecem, desde que o CPF e no mínimo um dado de contato sejam parametrizados no Create a Consent (mesma exceção da jornada completa).
- Resumo (4.2) e checklist (7.2) da jornada reduzida. O modo validação passa a considerar o tipo de jornada.

### Alterado
- Link do Portal Klavi nos disclaimers: `https://portal.klavi.ai/`. Na validação, `https://portal-open.klavi.ai/login` (endereço antigo do mesmo portal) também é aceito.

### Inalterado
- Requisitos da jornada completa. Seleção de Instituição (5.2) e Redirecionamento (5.4) são compartilhados pelas duas jornadas.

## [1.0.0] - 2026-09-10
### Adicionado
- Versão inicial: 15 requisitos obrigatórios (REQ-LP-01 a REQ-RED-03) e checklist final.
- Modo validação (seção 8): validar telas já construídas a partir de capturas, Figma, código ou URL.
