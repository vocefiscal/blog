---
layout: post
title: Atualização de progresso!
tags : [atualizacao-progresso]
---

Após duas semanas de muito trabalho após o primeiro turno, podemos compartilhar o progresso atual do projeto!

O tratamento inicial das imagens consistia em duas etapas: "costura" das fotos de um 
mesmo Boletim de Urna em uma foto única e extração da informação na imagem 
resultante através de reconhecimento de caracteres. O objetivo da costura é 
aprimorar a usabilidade, para produzir uma imagem única de fácil comparação 
visual com o Boletim de Urna eletrônico [publicado no site do TSE](http://www.tse.jus.br/eleicoes/eleicoes-2014/boletim-de-urna-na-web).
A extração de informação é a etapa mais crítica, pois permite verificar se as quantidades de 
votos são compatíveis entre Boletim de Urna impresso e eletrônico.

Para a primeira etapa, utlizamos o algoritmo de costura da biblioteca em código 
aberto [OpenCV](http://opencv.org/). Os resultados preliminares foram animadores 
e gerados rapidamente para Boletins de Urna compostos por poucas imagens, conforme imagem abaixo.

![](https://raw.githubusercontent.com/vocefiscal/vocefiscal-backend/master/samples/stitched.jpg)

Entretanto, o desempenho cai assustadoramente para Boletins 
de Urna compostos por muitas fotos, pois o OpenCV tenta todas as combinações 
possíveis para encaixar as fotos.  Após alguns ajustes, forçamos a implementação 
a tentar encaixar apenas as fotos em ordem, mas a ausência de textura na 
sobreposição dificulta o cálculo de similaridade entre fotos consecutivas. 
Descobrimos, portanto, que os algoritmos atuais de costura são mais orientados a 
textura e a sobreposição de texto simples entre duas fotos não parece 
suficiente. Continuamos trabalhando nessa direção!

Para a segunda etapa de reconhecimento de caracteres, estamos utilizando o motor 
de código aberto [Tesseract](https://code.google.com/p/tesseract-ocr/), treinado 
especificamente para a fonte da urna eletrônica. Os arquivos de treinamento 
estão no [repositório](https://github.com/vocefiscal/vocefiscal-backend). Em primeiro lugar, 
aplicamos binarização como pré-processamento, para destacar o texto do fundo.

<img src="https://raw.githubusercontent.com/vocefiscal/vocefiscal-backend/master/samples/00.jpg" width="200">
<img src="https://raw.githubusercontent.com/vocefiscal/vocefiscal-backend/master/samples/00-binary.jpg" width="200">

Após o pré-processamento, o reconhecimento de caracteres é capaz de recuperar a maior parte do texto na 
imagem, especialmente quando o treinamento é realizado com imagens já 
binarizadas:

```
Justiça Eleitorall
Tribunal Regional Eleitoral [sp]
Boletim de Urna
Eleições Gerais 2014
iº Turno
(05/10/2014)
Município 63134
CARAPlCUlBA
Zona Eleitoral 0303
Local de Votação 1384
Seção Eleitoral 0379
Eleitores aptos 0340
Comparecimento 0274
Eleitores faltosos 0066
Código identificação UE 01564145
Data de abertura da UE 05/10/2014
Horário de abertura 08:00 00
Data de fechamento da UE 05/10/2014
Horário de fechamento 17:01:01
RESUMO DA CORRESPONDÊNClA
630:382
Código Verificador: 68950
```

Utilizamos esse procedimento para fazer uma triagem e organizar a base de 
imagens recebida pelo aplicativo. Para cada Boletim de Urna recebido, utilizamos 
reconhecimento de caracteres para recuperar o resumo da correspondência na 
primeira foto. Caso encontrado, é possível obter o número da zona e seção 
corretos a partir da base de [correspondências efetivadas do TSE](http://www.tse.jus.br/eleicoes/estatisticas/repositorio-de-dados-eleitorais). 
Utilizamos um programa bem simples em Python para verificar se os dados 
preenchidos pelos usuários são compatíveis com as informações recuperadas a 
partir do resumo da correspondência. Em caso negativo ou se a correspondência 
não for encontrada, o programa apresenta a imagem e solicita tratamento manual. 
Por isso, o procedimento é semi-automático e toma bastante tempo para uma base grande.

Como resultado, fomos capazes de confirmar a origem de 7671 dos 11530 Boletins 
de Urna recebidos, que seguem agora para extração das demais informações. 
Inúmeros erros de preenchimento foram corrigidos, produzindo portanto três bases 
distintas, disponíveis no [repositório](https://github.com/vocefiscal/vocefiscal-backend). A primeira base (**base-original.zip**)
contém os metadados brutos, apenas anonimizados. A segunda base (**base-corrigida.zip**) contém os 
metadados separados após triagem e correção de erros de preenchimento. A 
terceira base (**base-organizada.zip**) contém os metadados organizados por município/zona/seção 
eleitoral. Os Boletins de Urna cuja origem não foi confirmada ainda não foram 
descartados, mas precisarão de outra estratégia de confirmação, possivelmente o 
código de carga impresso no final do documento. As estatísticas de submissão por 
estado podem ser encontradas abaixo, onde a última coluna exibe quantas submissões daquele estado tiveram
origem confirmada:

|UF|TOTAL |OK  |
|:-|:----:|:--:|
|AC|8     |8   |
|AL|45    |41  |
|AM|51    |19  |
|AP|11    |10  |
|BA|231   |154 |
|CE|135   |101 |
|DF|1023  |751 |
|ES|304   |245 |
|GO|429   |282 |
|MA|69    |44  |
|MG|1334  |973 |
|MS|193   |127 |
|MT|164   |117 |
|PA|105   |81  |
|PB|52    |33  |
|PE|223   |179 |
|PI|30    |20  |
|PR|961   |653 |
|RJ|733   |522 |
|RN|77    |54  |
|RO|61    |14  |
|RR|6     |5   |
|RS|532   |397 |
|SC|825   |618 |
|SE|38    |23  |
|SP|3249  |2102|
|TO|66    |30  |
|ZZ|71    |68  |
