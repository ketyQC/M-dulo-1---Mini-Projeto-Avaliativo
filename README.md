## Mini projeto de vendas de Halloween — Festa em Cena
Este mini projeto foi feito para limpar, organizar e analisar uma tabela de vendas de Halloween da empresa **Festa em Cena**, utilizando python e a biblioteca pandas
## Descrição do projeto e objetivo
*   **O Problema**: A Festa em Cena possuía uma base de dados com erros numéricos, falta de padronização em textos como os acentos de exclamação nas categorias e datas inconsistentes.
*   **O Objetivo**: Criar um programa que higienize esses dados, organize os arquivos em pastas e valide hipóteses operacionais para gerar um relatório confiável, preservando o arquivo original.
## Estrutura dos Dados
*   **Significado de uma linha**: Cada linha no arquivo representa um **item de um pedido individual** feito por clientes.
*   **Significado das 4 colunas escolhidas**:
    *   `pedido_id`: O número de identificação da compra.
    *   `categoria`: O tipo de produto.
    *   `canal_venda`: O canal onde o produto foi comprado Web, Loja física, Mercado.
    *   `data_venda`: O dia e a hora em que foi realizadp o pedido.
## Organização das pastas
Criei pastas no projeto para melhorar a organização do material:
*   `data/`: Onde fica o arquivo bruto original (`halloween_vendas.csv`).
*   `notebooks/`: Onde fica o código de análise que criei (`analise_final_halloween.ipynb`).
*   `output/`: Onde salvei o resultado final tratado (`pedidos_halloween_finais.csv`).
## Regras que usei e justificativas
### 1. Sprint 1 - Configuração e Ingestão
*   **Quantidade**: Deve ser maior que 0.
*   **Preço**: Deve estar preenchido e não pode ser negativo.
*   **Ação realizada**: Se a linha tiver erro, o código apenas conta o problema em vez de inventar ou colocar um valor qualquer no lugar, mantendo a resultado real dos dados.
### 2. Sprint 2 - Transformação de Strings
*   **Categoria**: Se estava vazia, o sistema escreve `"sem categoria"`. Usei o comando `re.sub` com expressões regulares para apagar os pontos de exclamação (`!`) e deixar tudo em letra minúscula.
*   **Canal de vendas**: O código padroniza tudo para apenas três nomes oficiais, sem acréscimos de acentos ou espaços no início/fim: `Web`, `Loja física` e `Mercado`.
### 3. Sprint 3 - Nulos e Validação (Análise da Hipótese)
*   **Hipótese testada**: Analisar se todo pedido sem data de entrega estava com o status "Cancelado".
*   **Conclusão**: Descobri que essa informação é **FALSA**. O código provou que existem 34 pedidos com status "Concluído" que também não têm a data de entrega preenchida.
### 4. Sprint 4 - Regras de Negócio e Datas
*   **Formato**: Realizei a conversão das datas do arquivo original usando a biblioteca `datetime` para o formato de apresentação do Brasil (`dia/mês/ano`).
*   **Conclusão**: Se a data de venda estava inválida ou vazia, o código apenas pulou o registro na contagem de tempo para continuar a execução.
