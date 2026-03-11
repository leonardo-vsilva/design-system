# Linkana Design System

## Visão geral

Design system da Linkana baseado em shadcn/ui com ruby_ui (implementação Rails).
Stack: Ruby on Rails + Tailwind CSS v4 + ruby_ui + tw-animate-css.

## Princípios

- **Consistência acima de criatividade.** Prefira componentes existentes a soluções ad-hoc.
- **Sem customizações de cor.** Nunca adicione cores fora dos tokens definidos.
- **dark mode sempre.** Todos os componentes devem funcionar nos dois temas.
- **Semântica primeiro.** Use o componente correto para o contexto correto — não use Button para navegação, use Link.

## Tema

O tema da Linkana é neutro/acromático. A paleta primária é preto/branco com escala de cinzas.
Cores com matiz aparecem apenas em: destructive (vermelho), warning (âmbar), success (verde) e charts.

Suporte a dark mode via classe `.dark` no elemento pai.

## Estrutura desta documentação

```
tokens/
  colors.md       — tokens de cor (CSS custom properties)
  typography.md   — fonte, tamanhos, pesos
  radius.md       — escala de border-radius
  spacing.md      — espaçamento e container

components/
  [nome].md       — documentação de cada componente shadcn/ruby_ui

patterns/
  forms.md        — padrões de composição de formulários
```

## Como consultar

- Para tokens de cor: veja `tokens/colors.md`
- Para usar um componente: veja `components/[nome].md`
- Para montar formulários: veja `patterns/forms.md`

## Decisores

Leo, Cidão. PRs de mudança estrutural no design system passam por eles.

## Biblioteca de referência

- shadcn/ui: https://ui.shadcn.com/docs/components
- ruby_ui: https://ruby-ui.com
- Tailwind CSS v4: https://tailwindcss.com/docs
