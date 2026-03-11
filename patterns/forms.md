# Padrões de Formulário

## Estrutura padrão de formulário

Todo formulário da Linkana segue esta hierarquia:

```
1. Título da seção (opcional, quando há múltiplas seções)
2. Campos agrupados logicamente
3. Texto de ajuda (opcional)
4. Ações (Submit + Cancelar)
```

## Layout de campos

### Coluna única (padrão)
Para formulários simples ou em modais:
```erb
<div class="flex flex-col gap-4">
  <%# campo 1 %>
  <%# campo 2 %>
  <%# campo 3 %>
</div>
```

### Duas colunas (formulários de entidade)
Para formulários com muitos campos em página dedicada:
```erb
<div class="grid grid-cols-2 gap-4">
  <%# campos pareados %>
</div>
```

## Anatomia de um campo

```erb
<div class="flex flex-col gap-1.5">
  <%= render RubyUI::Label.new(for: "field_id") { "Label do campo *" } %>
  <%= render RubyUI::Input.new(id: "field_id", name: "model[field]", placeholder: "ex: valor de exemplo") %>
  <p class="text-sm text-muted-foreground">Descrição auxiliar opcional.</p>
  <%# Mensagem de erro (apenas quando inválido): %>
  <%# <p class="text-sm text-destructive">Mensagem de erro.</p> %>
</div>
```

## Seções de formulário

Quando o formulário tem múltiplos grupos de campos:

```erb
<div class="flex flex-col gap-8">
  <section>
    <h3 class="text-base font-semibold mb-4">Dados da empresa</h3>
    <div class="flex flex-col gap-4">
      <%# campos da seção %>
    </div>
  </section>
  <%= render RubyUI::Separator.new %>
  <section>
    <h3 class="text-base font-semibold mb-4">Endereço</h3>
    <div class="flex flex-col gap-4">
      <%# campos da seção %>
    </div>
  </section>
</div>
```

## Ações do formulário

```erb
<div class="flex items-center justify-end gap-3 pt-4 border-t">
  <%= render RubyUI::Button.new(variant: :outline) { "Cancelar" } %>
  <%= render RubyUI::Button.new(type: :submit) { "Salvar" } %>
</div>
```

## Regras gerais

- ✅ Campos obrigatórios marcados com `*` no label.
- ✅ Erros de validação exibidos inline abaixo do campo, em `text-sm text-destructive`.
- ✅ Botão de submit desabilitado durante processamento (loading state).
- ✅ Ordenação de campos: mais importantes primeiro; do geral para o específico.
- ✅ Agrupe campos relacionados (ex: todos os campos de endereço juntos).
- ✅ `gap-4` entre campos, `gap-8` entre seções.
- ❌ Não use mais de 2 colunas em formulários dentro de modais.
- ❌ Não misture layouts de coluna única e duas colunas no mesmo grupo de campos.
- ❌ Não coloque ações (botões) no meio do formulário — sempre no final.
- ❌ Não use `placeholder` como substituto do `label`.

## Tipos de campo por dado

| Dado | Componente |
|------|-----------|
| Texto curto (nome, email) | `Input` |
| Texto longo (descrição, observação) | `Textarea` |
| Seleção de lista fixa pequena (< 10) | `Select` |
| Seleção com busca / lista longa | `Combobox` |
| Data | `DatePicker` |
| Range de datas | `DatePicker` com `mode: :range` |
| Booleano em formulário | `Checkbox` |
| Toggle imediato (sem submit) | `Switch` |
| Escolha exclusiva visível (2-5 opções) | `RadioGroup` |
| Código OTP | `InputOTP` |
| Número com range | `Slider` |

## Formulários em modal (Dialog)

- Máximo de 6 campos por modal.
- Uma coluna apenas.
- Ações no `DialogFooter`.

## Formulários em Sheet

- Até 12 campos.
- Pode usar 2 colunas para campos curtos.
- Ações no `SheetFooter`.

## Formulários em página dedicada

- Sem limite de campos.
- Use seções com separadores.
- Ações fixas no rodapé ou sticky no topo.
