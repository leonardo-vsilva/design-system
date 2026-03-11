---
title: "Radius"
---

## Scale

Base: `--radius: 0.625rem` (10px)

| Token         | Valor calculado        | Classe Tailwind | Uso típico                 |
| ------------- | ---------------------- | --------------- | -------------------------- |
| `--radius-sm` | ~6px (0.625rem - 4px)  | `rounded-sm`    | Badges, tags pequenas      |
| `--radius-md` | ~8px (0.625rem - 2px)  | `rounded-md`    | Inputs, botões             |
| `--radius-lg` | 10px (0.625rem)        | `rounded-lg`    | Cards, popovers, dropdowns |
| `--radius-xl` | ~14px (0.625rem + 4px) | `rounded-xl`    | Modals, sheets, drawers    |

---

## Regras

- ✅ Botões: `rounded-md`
- ✅ Inputs e selects: `rounded-md`
- ✅ Cards: `rounded-lg`
- ✅ Popovers e dropdowns: `rounded-lg`
- ✅ Modals (Dialog, Sheet, Drawer): `rounded-xl`
- ✅ Badges e tags: `rounded-sm` ou `rounded-full` para pills
- ❌ Não use valores arbitrários de radius (ex: `rounded-[12px]`).
- ❌ Não use `rounded-none` exceto em bordas internas de tabelas.