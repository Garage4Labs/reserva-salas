# reserva-salas · projeto-modelo da disciplina

API de reserva de salas, pequena de propósito, para praticar engenharia de software com agentes de IA.
Serve para qualquer ferramenta: Claude Code, GitHub Copilot, Gemini CLI ou outra.

## Começar em 3 minutos
```bash
# 1. Copie esta pasta para o repositório do seu grupo (ou use o repositório-modelo da turma)
# 2. Node.js 20 ou mais novo:
node --version
# 3. Rode os testes (não há nada para instalar):
npm test
# 4. Suba a API e abra http://localhost:3000/salas
npm start
# 5. Ligue o hook de git que bloqueia segredo e teste quebrado:
npm run hooks:git
```

Testar na mão (outro terminal):
```bash
curl -X POST http://localhost:3000/reservas -H "content-type: application/json" \
  -d '{"sala":"lab-1","inicio":"2026-12-01T14:00:00-03:00","fim":"2026-12-01T16:00:00-03:00","responsavel":"prof.ana"}'
```

## O que tem aqui
| Arquivo | Para que serve | Aula |
|---|---|---|
| `AGENTS.md` | Contexto do projeto para qualquer agente | 1 e 2 |
| `CLAUDE.md`, `GEMINI.md`, `.github/copilot-instructions.md` | Apontam cada ferramenta para o `AGENTS.md` | 1 e 2 |
| `docs/specs/SPEC-001-reservar-sala.md` | A SPEC com os critérios dos labs | 1 a 3 |
| `docs/specs/_modelo-spec.md` | Modelo para as próximas SPECs | 2 |
| `.claude/skills/escrever-teste/` e `.claude/commands/revisar-spec.md` | Skill e comando de exemplo | 2 |
| `.claude/settings.json` e `scripts/bloqueia-segredo.js` | Hook do Claude Code que bloqueia segredo | 3 |
| `.githooks/pre-commit` | O mesmo bloqueio, para qualquer ferramenta | 3 |
| `.github/workflows/ci.yml` e `revisao-ia.yml` | CI e revisão automática do PR | 3 |
| `.claude/agents/` | Subagentes planejador, construtor e revisor | 4 |
| `docs/fluxo-exemplo.yaml` | Fluxo da mini-fábrica | 4 |
| `docs/licoes/_modelo-licao.md` e `diario/DIARIO.md` | Lições e diário de bordo | todas |

## O que falta (é o trabalho de vocês)
- **Lab 1:** CA-3, reserva no passado é recusada.
- **Lab 2:** SPEC-002, cancelar reserva (só escrever e criticar, sem código).
- **Lab 3:** CA-2, conflito de horário, com o teste antes do código.
- **Lab 4:** implementar a SPEC-002 passando pelo fluxo da mini-fábrica.

Os grupos com tema próprio seguem os mesmos passos no projeto deles e usam este como referência.
