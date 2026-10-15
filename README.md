# Dashboard de Vendas Porsche

Dashboard interativa desenvolvida como projeto educacional da DIO. A aplicação transforma uma planilha com 100 registros de vendas em indicadores, gráficos e filtros para explorar os resultados.

🔗 [Acessar a dashboard](https://fellipemec.github.io/dashboard_porsche_sales/)

## Perguntas de negócio

1. **Quais modelos geram mais receita?**  
   Identifica quais modelos mais contribuem para o faturamento, apoiando a análise do portfólio.

2. **Quais estados concentram mais vendas?**  
   Mostra a distribuição das vendas e os mercados com maior volume de registros.

3. **Quais formas de pagamento são mais usadas?**  
   Permite entender a distribuição dos meios de pagamento registrados na base.

Cada pergunta é respondida por um gráfico de barras, atualizado conforme os filtros selecionados.

## Funcionalidades

- Indicadores de quantidade de vendas, receita total, ticket médio e estados atendidos.
- Filtros por modelo, estado, cidade, ano da venda, ano do modelo e pagamento.
- Botão para limpar os filtros.
- Tabela com os registros do recorte selecionado.
- Exportação dos dados filtrados em CSV.
- Layout responsivo, com paleta em preto, branco e vermelho e tipografia Arial.
- Funcionamento sem internet após baixar o HTML.

## Base de dados e tratamento

Foi utilizada a planilha `Planilha-porcher.xlsx`, na aba `Sanitized`, com 100 registros.

O tratamento incluiu:

- Seleção das colunas sanitizadas de data, modelo, ano do modelo, preço, pagamento, cidade e estado.
- Preservação do identificador de cada venda.
- Conversão de preço e ano do modelo para números.
- Incorporação dos dados como valores no HTML, sem depender de fórmulas do Excel.
- Exclusão dos nomes de clientes e vendedores do conteúdo da dashboard.

A base contém 24 datas marcadas como `INVALID`. Esses registros foram preservados nos totais gerais e identificados como “Data inválida”. Quando um ano da venda é selecionado, entram apenas os registros com datas válidas daquele ano.

Os preços foram mantidos em dólares americanos (USD). Datas futuras presentes na planilha também foram preservadas, sem presumir que representam vendas já realizadas.

Os dados necessários estão incorporados no `index.html`. A planilha original não é necessária para executar a dashboard.

## Definição dos indicadores

- **Vendas:** quantidade de registros no recorte.
- **Receita total:** soma dos preços registrados.
- **Ticket médio:** receita total dividida pela quantidade de vendas.
- **Estados atendidos:** quantidade de estados distintos no recorte.

A receita não representa lucro e não considera dedução de custos ou confirmação de entrega.

## Uso da inteligência artificial

O projeto foi desenvolvido com auxílio do Codex, utilizando skills de planilhas e sites para analisar a base e construir o HTML.

Não foi utilizado o Canvas nem criado um agente personalizado. A ferramenta auxiliou na preparação dos dados, escolha das perguntas, implementação e verificação da lógica dos filtros.

A publicação no GitHub Pages foi realizada por mim.

## Prompt e refinamentos

O pedido inicial foi:

> Crie uma dashboard em HTML, em arquivo único, usando a planilha de vendas Porsche. Escolha três perguntas de negócio, cada uma respondida por um gráfico ou indicador. Inclua filtros por campos como modelo, cidade, ano ou método de pagamento, indicadores de total de vendas e receita e um visual coerente. Faça apenas a dashboard; a publicação no GitHub será realizada por mim.

Esse texto resume a solicitação usada na conversa.

Durante a implementação, foram definidas as três perguntas de negócio e adotados os seguintes ajustes:

- Separação entre ano da venda e ano do modelo.
- Preservação dos registros com datas inválidas.
- Identificação explícita da moeda como USD.
- Inclusão de tabela detalhada e exportação em CSV.
- Tratamento de combinações de filtros sem resultados.
- Incorporação dos dados, estilos e scripts no próprio HTML.

## Tecnologias

- HTML
- CSS
- JavaScript
- GitHub Pages

A dashboard está concentrada no arquivo `index.html` e não depende de bibliotecas externas.

## Verificação

Foram conferidos os 100 registros e a receita total de US$ 12.827.800,50.

A lógica foi testada para as opções dos seis filtros, seleção de datas inválidas, combinação sem resultados e limpeza dos filtros.

## Como executar

### Online

Acesse a [dashboard publicada](https://fellipemec.github.io/dashboard_porsche_sales/).

### No computador

1. Baixe o arquivo `index.html` deste repositório.
2. Abra o arquivo em um navegador.
3. Utilize os filtros para explorar os dados.

Não é necessário instalar dependências nem iniciar um servidor.

## Capturas de tela

### Visão geral

<img width="1402" height="690" alt="Visão geral da dashboard de vendas Porsche" src="https://github.com/user-attachments/assets/b06ffb4b-8256-4091-971e-ad5ab2ba5c8d" />

### Detalhe da dashboard

<img width="1470" height="728" alt="Segunda captura da dashboard de vendas Porsche" src="https://github.com/user-attachments/assets/4c32a20f-fcad-41c2-8c94-f8f05f33a25c" />

## Sobre o projeto

Projeto educacional desenvolvido para praticar análise de dados, construção de dashboards com apoio de IA e publicação na web.

Não possui vínculo oficial com a Porsche.
