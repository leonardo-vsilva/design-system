# Tokens de Espaçamento

O espaçamento usa a escala padrão do Tailwind (base 4px). Nenhuma escala customizada foi adicionada.

## Escala de referência (mais usados)

| Classe | Valor | Uso típico |
|--------|-------|-----------|
| `p-1` / `m-1` | 4px | Espaçamento interno mínimo (ícones, badges) |
| `p-2` / `m-2` | 8px | Padding de inputs compactos |
| `p-3` / `m-3` | 12px | Padding de badges, tags |
| `p-4` / `m-4` | 16px | Padding padrão de cards, seções |
| `p-6` / `m-6` | 24px | Padding de modais, painéis |
| `p-8` / `m-8` | 32px | Padding de páginas |
| `gap-2` | 8px | Espaço entre elementos inline |
| `gap-4` | 16px | Espaço entre campos de formulário |
| `gap-6` | 24px | Espaço entre seções |

## Container

Definido via `@utility container`:

```
margin-inline: auto
padding-inline: 2rem (32px)
max-width: 1400px
```

Aplicado com a classe `container`.

## Regras

- ✅ Use múltiplos de 4 (escala Tailwind padrão).
- ✅ Padding interno de cards: `p-4` ou `p-6`.
- ✅ Gap entre campos de form: `gap-4`.
- ✅ Gap entre itens de lista/nav: `gap-2`.
- ❌ Não use valores arbitrários (ex: `p-[13px]`) — ajuste para o múltiplo mais próximo.
- ❌ Não use `margin: auto` manual — use `container` ou flexbox/grid.
