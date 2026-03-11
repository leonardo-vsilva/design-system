# Tokens de Tipografia

## Família de fonte

Stack de fontes do sistema (system font stack). Definida diretamente no `body`:

```
-apple-system, BlinkMacSystemFont, "Segoe UI", "Helvetica Neue", Roboto, Arial, sans-serif,
"Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol"
```

Nenhuma fonte customizada (Google Fonts, etc.) está em uso. O objetivo é renderização nativa e performática em cada plataforma.

## Escala de tamanhos (Tailwind padrão)

| Classe | Tamanho | Uso típico |
|--------|---------|-----------|
| `text-xs` | 12px | Labels auxiliares, badges, metadados |
| `text-sm` | 14px | Corpo de texto padrão em UI, labels de form |
| `text-base` | 16px | Texto corrido, descrições |
| `text-lg` | 18px | Títulos de seção menores |
| `text-xl` | 20px | Títulos de cards |
| `text-2xl` | 24px | Títulos de página |
| `text-3xl` | 30px | Headings maiores |

## Pesos

| Classe | Peso | Uso típico |
|--------|------|-----------|
| `font-normal` | 400 | Texto corrido |
| `font-medium` | 500 | Labels, botões, nav items |
| `font-semibold` | 600 | Títulos de cards, headings secundários |
| `font-bold` | 700 | Headings principais |

## Cores de texto

Use sempre tokens semânticos — nunca cores hardcoded:

| Classe | Token | Uso |
|--------|-------|-----|
| `text-foreground` | `--foreground` | Texto principal |
| `text-muted-foreground` | `--muted-foreground` | Texto auxiliar, placeholders, labels secundárias |
| `text-primary` | `--primary` | Destaque de texto com cor primária |
| `text-destructive` | `--destructive` | Mensagens de erro |
| `text-warning` | `--warning` | Alertas |
| `text-success` | `--success` | Confirmações |

## Regras

- ✅ Texto padrão de interface: `text-sm font-medium text-foreground`
- ✅ Labels auxiliares: `text-xs text-muted-foreground`
- ✅ Títulos de card: `text-base font-semibold`
- ✅ Títulos de página: `text-2xl font-bold`
- ❌ Não use tamanhos acima de `text-3xl` em UI de produto.
- ❌ Não use `font-black` (900) — fora da escala do sistema.
