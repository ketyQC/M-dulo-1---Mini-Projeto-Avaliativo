# Mini projeto de vendas de Halloween
Este mini projeto foi feito para limpar, organizar e analisar uma tabela de vendas de Halloween usando python e pandas.
## Criei pastas no projeto, para melhor organização
* `data/`: onde fica o arquivo bruto original (`halloween_vendas.csv`).
* `notebooks/`: onde fica o código que criei (`analise_final_halloween.ipynb`).
* `output/`: onde salvei o resultado final(`pedidos_halloween_finais.csv`).
## Regras que usei e justificativas
### 1. Sprint 1 - Configuração e Ingestão
* Quantidade: Deve ser maior que 0.
* Preço: Deve ser preenchido e não pode ser negativo.
* Realizado: Se a linha tiver erro, apenas contar o problema em vez de inventar colocar um valor qualquer no lugar.
### 2. Sprint 2 - Transformação de Strings
* Categoria: Se estava vazia, escrever "sem categoria". Usei o comando re.sub para apagar os pontos de exclamação (`!`) e deixar tudo em letra minúscula.
* Canal de Venda: Apenas três nomes padrão foram identificados, sem acréscimos de acentos ou espaçamento: `Web`, `Loja física` e `Mercado`.
### 3. Sprint 3 - Nulos e Validação
* Após análise dos dados percebi que todo pedido sem data de entrega estava Cancelado".
* Conclui que esta informação é FALSO, porque existem vários pedidos com status "Concluído" que também não têm a data de entrega preenchida.
### 4. Sprint 4 - Regras de Negócio e Datas
* Formato: Realizei a conversão das datas do arquivo original para o formato do Brasil (dia/mês/ano).
* Se a data estava invalida ou vazia, apenas pulei para continuar o código.
