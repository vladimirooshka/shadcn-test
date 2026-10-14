# shadcn-test

Песочница для проектирования интерфейсов агентом на компонентах shadcn/ui.

## Первый запуск

```bash
# 1. Создать приложение (Next.js + shadcn) в папке web/
npx shadcn@latest init -t next -n web --no-monorepo

# CLI создаёт внутри web/ свой git-репозиторий, он здесь не нужен
rm -rf web/.git            # Windows cmd: rmdir /s /q web\.git

# 2. Проверить, что всё собралось
cd web && npm run dev
```

После шага 1 в `web/` появятся `components.json`, тема и компонент `button`.

## MCP

`.mcp.json` в корне уже подключает MCP-сервер shadcn для Claude Code. Открой проект в Claude Code, подтверди сервер и проверь командой `/mcp`: shadcn должен быть `Connected`.

Для других клиентов: `npx shadcn@latest mcp init --client cursor` (или `vscode`, `codex`), см. https://ui.shadcn.com/docs/mcp

## CLI

```bash
npx shadcn@latest search @shadcn -q "login"   # найти компоненты и блоки
npx shadcn@latest view @shadcn/login-03       # посмотреть код
npx shadcn@latest add card dialog --cwd web   # добавить в проект
```
