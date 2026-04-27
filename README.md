# .github

Repositório de configuração organizacional da [rfidcheckout](https://github.com/rfidcheckout). Centraliza templates, workflows reutilizáveis e padrões compartilhados entre todos os repositórios do projeto.

## Conteúdo

### Perfil da organização

- [`profile/README.md`](profile/README.md) — página de perfil exibida em `github.com/rfidcheckout`

### Issue templates

- [`bug.yml`](.github/ISSUE_TEMPLATE/bug.yml) — relatório de bug
- [`feature.yml`](.github/ISSUE_TEMPLATE/feature.yml) — nova funcionalidade
- [`chore.yml`](.github/ISSUE_TEMPLATE/chore.yml) — manutenção e infraestrutura

### PR template

- [`pull_request_template.md`](.github/pull_request_template.md) — template padrão para pull requests

### Workflows reutilizáveis

- [`pr-lint.yml`](.github/workflows/pr-lint.yml) — valida título de PR no formato `[ISSUE-ID - ]<type>: <description>`
- [`label-sync.yml`](.github/workflows/label-sync.yml) — sincroniza labels do [`labels.yml`](labels.yml) para todos os repos da org
- [`repo-config-sync.yml`](.github/workflows/repo-config-sync.yml) — configura repo settings (squash only, auto-delete branch) e branch protection (require PR, 1 approval)
- [`dependabot-sync.yml`](.github/workflows/dependabot-sync.yml) — sincroniza configs do [`dependabot/`](dependabot/) para todos os repos da org

### Labels

- [`labels.yml`](labels.yml) — fonte canônica de labels (tipo, escopo, prioridade, tamanho)

### Dependabot

- [`dependabot/architecture.yml`](dependabot/architecture.yml) — GitHub Actions
- [`dependabot/backend.yml`](dependabot/backend.yml) — GitHub Actions + Go
- [`dependabot/frontend.yml`](dependabot/frontend.yml) — GitHub Actions + npm
