# Relatório: matérias-primas com estoque positivo e preço zerado

Data: 2026-10-14 · Fonte: tabela `materiaprima_produtos` (Supabase)

## Resumo
- Matérias-primas cadastradas: **182**
- Com estoque positivo: **127**
- Com estoque > 0 e **preço de custo e preço médio zerados**: **16** (12,6% das com estoque)
- Caso parcial (só `preco_custo` zerado, `preco_medio` preenchido): **1** — MP-00070

## Lista (estoque > 0, preço custo = preço médio = 0)

| Código | Produto | Un. | Estoque | Entradas registradas | Observação |
|---|---|---|---|---|---|
| MP-00002 | Polpa de Açaí Congelado | Kg | 10,000 | 0 | |
| MP-00006 | Aroma de Guaraná | Kg | 30,400 | 0 | |
| MP-00007 | Base creme | Kg | 4,500 | 0 | |
| MP-00045 | Granola | Kg | 1,000 | 0 | |
| MP-00051 | Leite em pó integral | Kg | 50,000 | 1 | entrada com valor unitário 0 |
| MP-00061 | Maracujá sem sementes | Kg | 23,000 | 0 | |
| MP-00077 | Polidextrose Type II IMP | Kg | 25,000 | 0 | |
| MP-00084 | Vinagre | L | 750,000 | 0 | |
| MP-00088 | Nutty Caramelo Salgado | Kg | 8,200 | 0 | |
| MP-00118 | Cacau Callebaut | Kg | 75,000 | 1 | entrada com valor unitário 0; pré-cadastro da planilha de gelato |
| MP-00127 | Chocolate (Mocca) | Kg | 12,122 | 0 | pré-cadastro da planilha de gelato |
| MP-00128 | Crockolosi Meringa | Kg | 3,200 | 2 | entradas com valor unitário 0; pré-cadastro da planilha de gelato |
| MP-00169 | Água de coco | Kg | 30,000 | 0 | |
| MP-00172 | Coco Seco - fresco em escama | Sc | 6,000 | 0 | |
| MP-00173 | Stracciatela Caramelo Salgado | Kg | 14,000 | 0 | |
| MP-00182 | Palito Hélice - Luna | Un | 29.000,000 | 0 | |

## Caso parcial
| Código | Produto | Un. | Estoque | Preço custo | Preço médio | Valor em estoque |
|---|---|---|---|---|---|---|
| MP-00070 | Texfair ICE 710 | Kg | 25,000 | 0,00 | 87,30 | 2.182,50 |

## Observações
- Todos os 16 itens têm `valor_estoque` = R$ 0,00, ou seja, o valor total do estoque está subavaliado.
- 13 dos 16 itens não têm nenhuma entrada em `materiaprima_entradas` (estoque provavelmente lançado direto no cadastro), por isso não há valor unitário de NF para recuperar.
- Os 3 que têm entradas (MP-00051, MP-00118, MP-00128) foram lançados com valor unitário 0.
- Maior impacto de quantidade: Vinagre (750 L) e Palito Hélice - Luna (29.000 Un).
