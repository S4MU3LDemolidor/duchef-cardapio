# DuChef Pizzaria · Cardápio online

Site: https://s4mu3ldemolidor.github.io/duchef-cardapio/

O cliente escolhe as pizzas no celular, monta o pedido (meio a meio, borda, adicionais, sabor da bebida) e envia já escrito no WhatsApp da pizzaria. Funciona na mesa (pelo QR code), para retirar e para entrega.

## Como mudar preços, sabores e horários

Tudo fica na planilha do Google **"DuChef · Cardápio do site"**:
https://docs.google.com/spreadsheets/d/1FjtC2pEAFUCsaZ6s3KuIIkocutg6NngsPZpaC3tRS48/edit

Edite a planilha e pronto: o site lê os dados toda vez que alguém abre a página. Não precisa mexer no código. A aba **Como usar** explica cada coluna.

| Aba | O que tem |
|---|---|
| Cardápio | Uma linha por item: preços por tamanho (pizzas) ou preço único (bebidas), opções de sabor, foto, etiqueta, "mais pedida" e "disponível" (esgotado) |
| Categorias | Subtítulo de cada categoria |
| Extras | Bordas recheadas e adicionais, com preço por tamanho |
| Bairros | Bairros atendidos e taxa de entrega de cada um (vazio = cliente digita o bairro) |
| Config | WhatsApp que recebe os pedidos, dias e horário, pedido mínimo, chave Pix, Instagram e faixa de aviso |

Cuidados:
- Não renomeie as abas nem os títulos da primeira linha.
- A planilha precisa continuar compartilhada como "Qualquer pessoa com o link pode ver". Só quem você convidar consegue editar.
- Se a planilha não carregar (sem internet, por exemplo), o site usa os dados guardados no próprio código (`DEF` em `index.html`).

## QR codes das mesas

Abra https://s4mu3ldemolidor.github.io/duchef-cardapio/mesas.html, escolha de qual mesa até qual e toque em **Imprimir** (ou "Salvar como PDF" para mandar à gráfica). São 6 por folha A4. Cada QR abre o cardápio com o número da mesa preenchido (`?mesa=7`).

## Fotos

As fotos ficam na pasta `img/` (formato `.webp`, 300×300, fundo transparente). Para colocar foto num item, envie o arquivo para `img/` e escreva o nome dele na coluna **Foto** da planilha. Itens sem foto mostram uma ilustração desenhada a partir dos ingredientes da descrição.

## Arquivos

- `index.html`: o cardápio
- `mesas.html`: gerador de QR codes para imprimir
- `img/`, `fonts/`, `icons/`: logo, fotos, fontes e ícones
- `og.jpg`: imagem que aparece quando o link é compartilhado no WhatsApp e no Instagram
- `manifest.webmanifest`: permite "Adicionar à tela inicial" no celular
