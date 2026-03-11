# Button

## O que é
Elemento de ação primária. Dispara uma ação quando clicado — submit de form, abertura de modal, execução de operação.

## Quando usar / quando NÃO usar
- ✅ Ações: salvar, confirmar, enviar, criar, deletar
- ✅ Abertura de modais, drawers, dialogs
- ❌ Navegação entre páginas — use link (`<a>`) ou Link component
- ❌ Ações secundárias de baixa importância — considere `ghost` ou `link` variant

## Variantes

| Variante | Uso | Aparência |
|----------|-----|-----------|
| `default` | Ação primária da página | Fundo preto, texto branco |
| `secondary` | Ação secundária | Fundo cinza claro, texto preto |
| `destructive` | Ação irreversível (deletar, remover) | Fundo vermelho |
| `outline` | Ação terciária com borda visível | Borda cinza, fundo transparente |
| `ghost` | Ação discreta, geralmente em toolbars | Sem borda, sem fundo — hover cinza |
| `link` | Ação que parece link de texto | Sem borda, sem fundo — underline |

## Tamanhos

| Size | Uso |
|------|-----|
| `default` | Tamanho padrão para a maioria dos contextos |
| `sm` | Contextos compactos (toolbars, tabelas) |
| `lg` | CTAs de destaque, páginas de onboarding |
| `icon` | Botão apenas com ícone (quadrado) |

## Regras
- ✅ Máximo de 1 botão `default` (primário) por seção/modal.
- ✅ Botões destrutivos sempre pedem confirmação via `AlertDialog` antes de executar.
- ✅ Use `size="icon"` com `aria-label` descritivo quando o botão contiver apenas ícone.
- ✅ Estado de loading: desabilite o botão e adicione spinner + texto "Carregando...".
- ❌ Não use `default` variant para ações secundárias.
- ❌ Não misture mais de 2 variantes diferentes num mesmo grupo de ações.

## Exemplos

✅ Correto — ação primária + secundária:
```erb
<%= render RubyUI::Button.new(variant: :default) { "Salvar" } %>
<%= render RubyUI::Button.new(variant: :outline) { "Cancelar" } %>
```

✅ Correto — ação destrutiva:
```erb
<%= render RubyUI::Button.new(variant: :destructive) { "Excluir fornecedor" } %>
```

❌ Errado — usar Button para navegação:
```erb
<%= render RubyUI::Button.new(href: "/suppliers") { "Ver fornecedores" } %>
```
