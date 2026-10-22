#  Relatório final das vendas
## Números da Qualidade dos Dados
Depois de realizar a analise das 1500 linhas do arquivo, foram encontradas as seguintes informações:
* **Categorias atualizadas:** 1482 linhas (18 estavam vazias e viraram "sem categoria").
* **Erros de Quantidade:** 7 linhas com problemas.
* **Erros de Preço:** 12 linhas com problemas.
* **Total de pedidos com algum erro numérico:** 19 pedidos no total.
* **Datas de venda com erro:** 4 datas inválidas.
* **Total de pedidos Cancelados:** 109 pedidos.
### Pedidos com divergência 
* Pedidos sem entrega que foram **Cancelados**: 109 pedidos.
* Pedidos sem entrega que estão com **Outros Status** ou **Vazia** sem informações: 34 pedidos.
* **Conclusão:** A hipótese é **FALSA**. Há 34 pedidos que deram como ‘Concluídos’, mas estão com divergência na data de entrega.
--
## Descobertas com os dados apurados
*Importante: Essas contagens mostram apenas os pedidos que foram criados no sistema, não significa o dinheiro que realmente faturou.*

### 1. Analise em relação aos canais de vendas
* **Web:** 666 pedidos.
* **Loja física:** 551 pedidos.
* **Mercado:** 283 pedidos.
* **Resultado:** O canal **Web** é o mais usado para realização das vendas. 
* **Porém:** Esse número conta até os pedidos que foram cancelados depois, então não reflete o lucro real.

### 2. Vendas por periodo
* **Outubro de 2024:** 393 pedidos.
* **Outubro de 2025:** 410 pedidos.
* **Resultado:** O mês de **Outubro** concentra quase todas as vendas por causa da data do Halloween - 31 de Outubro.
* **Porém:** Ter muitos pedidos em outubro não prova que a loja conseguiu entregar tudo dentro do prazo estipulado.
