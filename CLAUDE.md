# ReproSense-Setup — Instruções para o Claude

## Regras absolutas

- **NUNCA commitar sem permissão explícita.**
- Commits em português, formato convencional: `tipo(escopo): descrição`

---

## Projeto

Repositório que hospeda o instalador do Coletor Local ReproSense.
O arquivo principal é `ReproSense_Setup.exe` — **nunca renomear**.

Ao fazer push com `version.json` atualizado, uma GitHub Action sincroniza
automaticamente o `rmm/coletor_version.json` no repo `ReproSense` (Django),
fazendo o alerta de nova versão aparecer para todos os usuários logados.

---

## Fluxo ao receber uma nova versão do Coletor

O instalador `ReproSense_Setup.exe` é gerado no repo `ReproSense-Coletor`
e copiado para cá. O fluxo completo está documentado no CLAUDE.md do Coletor.

### Depois de copiar o novo instalador, fazer aqui:

**1. Atualizar `version.json`** com a mesma versão usada no Coletor:
```json
{"version": "2.2.0"}
```

**2. Commitar e dar push:**
```
chore: bump versão do Coletor para 2.2.0
```

A GitHub Action (`.github/workflows/sync-version.yml`) dispara automaticamente
e atualiza o alerta de versão no servidor Django — sem intervenção manual.

---

## Nome do instalador

O arquivo **deve sempre se chamar `ReproSense_Setup.exe`**.
O link de download no Django aponta para:
```
https://github.com/direquena/ReproSense-Setup/releases/latest/download/ReproSense_Setup.exe
```

Se o nome mudar, o download quebra para todos os usuários.
