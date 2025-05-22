## 🔖 Versionamento Semântico (X.Y.Z)

O projeto segue o padrão [SemVer 2.0.0](https://semver.org/), onde cada número representa:

```shell
X.Y.Z
│││
││└─ Z: PATCH (atualizações de correção)
││ └─ Incrementado quando: Correções de bugs, ajustes menores sem quebrar compatibilidade
││
│└── Y: MINOR (novas funcionalidades)
│ └─ Incrementado quando: Novas features são adicionadas de forma retrocompatível
│
└── X: MAJOR (mudanças significativas)
└─ Incrementado quando: Mudanças que quebram compatibilidade com versões anteriores
```

### Exemplos Práticos

| Mudança | Versão Anterior | Nova Versão | Motivo |
|---------|-----------------|-------------|--------|
| Correção de bug na exportação | 1.2.3 | 1.2.4 | Patch (Z) |
| Adição de suporte a novos formatos | 1.2.4 | 1.3.0 | Minor (Y) |
| Redesenho completo da API | 1.3.0 | 2.0.0 | Major (X) |
| Correção de segurança | 2.1.5 | 2.1.6 | Patch (Z) |

### Regras Adicionais

1. **Reset de contadores**
   - Quando Y aumenta, Z volta para 0
   - Quando X aumenta, ambos Y e Z voltam para 0

2. **Versão 0.Y.Z**:
   - Para desenvolvimento inicial (antes da versão 1.0.0)
   - Minor pode quebrar compatibilidade

3. **Metadata (opcional)**:
   - Pode-se adicionar sufixos como `-alpha`, `-beta`, `-rc1`
   - Exemplo: `2.1.0-beta.1`

### Quando Usar Cada Nível

- **PATCH (Z)**:
  - Correções de bugs críticos
  - Ajustes de performance menores
  - Atualizações de documentação

- **MINOR (Y)**:
  - Adição de novas funcionalidades
  - Melhorias retrocompatíveis
  - Depreciação de features (sem remoção)

- **MAJOR (X)**:
  - Mudanças arquiteturais significativas
  - Remoção de features depreciadas
  - Mudanças que exigem ação do usuário para migração

```mermaid
graph LR
    A[Commit] -->|Bug Fix| B(PATCH++)
    A -->|New Feature| C(MINOR++)
    A -->|Breaking Change| D(MAJOR++)
    B --> E{MINOR=0?}
    C --> F{MAJOR=0?}
    D --> G[Reset MINOR/PATCH]
