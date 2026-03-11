# Tokens de Cor

Definidos como CSS custom properties em `application.tailwind.css`.
Referenciados no Tailwind via `bg-primary`, `text-foreground`, etc.

## Paleta semântica (light mode)

| Token | Valor (oklch) | Uso |
|-------|--------------|-----|
| `--background` | oklch(1 0 0) | Fundo da página |
| `--foreground` | oklch(0.145 0 0) | Texto principal |
| `--card` | oklch(1 0 0) | Fundo de cards |
| `--card-foreground` | oklch(0.145 0 0) | Texto em cards |
| `--popover` | oklch(1 0 0) | Fundo de popovers/dropdowns |
| `--popover-foreground` | oklch(0.145 0 0) | Texto em popovers |
| `--primary` | oklch(0.205 0 0) | Cor primária — preto |
| `--primary-foreground` | oklch(0.985 0 0) | Texto sobre primary — branco |
| `--secondary` | oklch(0.97 0 0) | Cor secundária — cinza muito claro |
| `--secondary-foreground` | oklch(0.205 0 0) | Texto sobre secondary — preto |
| `--muted` | oklch(0.97 0 0) | Fundo de elementos silenciados |
| `--muted-foreground` | oklch(0.556 0 0) | Texto silenciado — cinza médio |
| `--accent` | oklch(0.97 0 0) | Fundo de estados hover/ativo leve |
| `--accent-foreground` | oklch(0.205 0 0) | Texto sobre accent |
| `--destructive` | oklch(0.577 0.245 27.325) | Erro / ação destrutiva — vermelho |
| `--destructive-foreground` | oklch(0.577 0.245 27.325) | Texto/ícone destrutivo |
| `--border` | oklch(0.922 0 0) | Bordas de inputs, cards, separadores |
| `--input` | oklch(0.922 0 0) | Fundo de bordas de input |
| `--ring` | oklch(0.708 0 0) | Outline de foco |

## Tokens de estado (ruby_ui)

| Token | Valor (hsl) | Uso |
|-------|-------------|-----|
| `--warning` | hsl(38 92% 50%) | Alertas de atenção — âmbar |
| `--warning-foreground` | hsl(0 0% 100%) | Texto sobre warning — branco |
| `--success` | hsl(87 100% 37%) | Confirmação / sucesso — verde |
| `--success-foreground` | hsl(0 0% 100%) | Texto sobre success — branco |

## Tokens de sidebar

| Token | Uso |
|-------|-----|
| `--sidebar` | Fundo da sidebar |
| `--sidebar-foreground` | Texto na sidebar |
| `--sidebar-primary` | Item ativo na sidebar |
| `--sidebar-primary-foreground` | Texto sobre item ativo |
| `--sidebar-accent` | Hover de items na sidebar |
| `--sidebar-accent-foreground` | Texto sobre hover |
| `--sidebar-border` | Bordas dentro da sidebar |
| `--sidebar-ring` | Foco dentro da sidebar |

## Tokens de charts

| Token | Valor | Uso |
|-------|-------|-----|
| `--chart-1` | oklch(0.646 0.222 41.116) | Laranja |
| `--chart-2` | oklch(0.6 0.118 184.704) | Teal |
| `--chart-3` | oklch(0.398 0.07 227.392) | Azul escuro |
| `--chart-4` | oklch(0.828 0.189 84.429) | Amarelo |
| `--chart-5` | oklch(0.769 0.188 70.08) | Amarelo-laranja |

## Dark mode

Ativado pela classe `.dark` no elemento pai (não pelo media query `prefers-color-scheme`).
Todos os tokens acima possuem equivalentes no escopo `.dark` em `application.tailwind.css`.

## Regras

- ❌ Nunca use cores hardcoded (ex: `text-gray-500`, `bg-red-500`) — use sempre os tokens semânticos.
- ❌ Nunca crie novos tokens de cor sem aprovação de Leo/Cidão.
- ✅ Use `text-muted-foreground` para textos secundários/labels auxiliares.
- ✅ Use `text-destructive` para mensagens de erro.
- ✅ Use `text-success` para confirmações.
- ✅ Use `text-warning` para alertas não-críticos.
