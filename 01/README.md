# Desafio 5.1: Análise de DEGs em Klebsiella pneumoniae

## Descrição do Desafio

Este desafio consistiu em investigar a resposta da bactéria resistente `Klebsiella pneumoniae` ao tratamento com `polimixina B`, sob estresse de alta concentração de íons de cálcio. 

Utilizando dados de um estudo publicado, o objetivo era identificar `quantos` e `quais genes` apresentavam `down-regulation` com um `fold-change inferior a -2.0`, e que fossem mapeados para a via metabólica de síntese do `peptidoglicano (ID: 00550)`.

## Nossa estratégia

Nossa solução para este desafio foi uma combinação de análise de dados e busca em bancos de dados biológicos, seguindo a seguinte metodologia:

### Filtro de Dados de Expressão
Processar o arquivo com os dados de DEGs ([ID_KO_KP.xls](dataset/ID_KO_KP.xls)) e aplicar o filtro de fold-change para identificar todos os genes com `logFC < -2.0`.

### Mapeamento KEGG
Utilizar o arquivo [ID_KO_KP.xls](dataset/ID_KO_KP.xls), que mapeia os IDs dos genes para os termos KO (KEGG Orthology), para identificar os genes que pertencem à via metabólica da síntese do peptidoglicano (mapID: 00550).

### Validação Cruzada
Intersectar a lista de genes down-regulated com a lista de genes da via metabólica do peptidoglicano.

### Geração de Relatório
O resultado final foi um arquivo de texto com a contagem total e o nome de cada um dos genes identificados.
