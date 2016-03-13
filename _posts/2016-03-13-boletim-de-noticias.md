---
layout: post
title: Boletim de Notícias
tags:
- "boletim-de-urna"
tagline: Faz muito tempo desde a última atualização, então fizemos um apanhado do que aconteceu desde então!
published: true
---

## Prêmios e repercussão internacional

O Projeto Você Fiscal foi [premiado em Novembro do ano passado](www.technologyreview.com.br/tr35/profile.aspx?trid=1632) pela edição brasileira da revista MIT Technology Review. O prêmio se chama Inovadores Menores de 35 anos Brasil e participar do evento foi muito interessante para estabelecer colaborações e discutir idéias para a evolução do projeto. Também tivemos a oportunidade de apresentar a iniciativa na conferência [Real World Cryptography 2016](http://realworldcrypto.com/rwc2016), com ótima repercussão entre os presentes. Os slides da apresentação podem ser encontrados no [site do evento](http://www.realworldcrypto.com/rwc2016/program/RWC16-DiegoAranha.pdf).

## Voto Impresso

O voto impresso foi aprovado para reintrodução nas eleições de 2018, após [longa tramitação](http://www12.senado.leg.br/noticias/materias/2015/12/28/eleicoes-terao-voto-impresso-a-partir-de-2018). Um dos pontos negativos do Projeto de Lei aprovado é a ausência de fases de auditoria e recontagem, que poderiam ter sido especificadas. Estamos nos aproximando de pesquisadores internacionais para estudar procedimentos que facilitem a adoção do recurso nas eleições brasileiras.

## Código QR e TPS

O TSE anunciou poucos dias após nossa última atualização a introdução de um código QR com assinatura digital nos Boletins de Urna das próximas eleições. Esse recurso deve facilitar em muito a aquisição de dados, pois toda a dificuldade com extração de informação via reconhecimento de caracteres torna-se trivial. O manual com a especificação [já foi publicado](http://www.tse.jus.br/eleicoes/eleicoes-2016/qr-code-no-boletim-de-urna-manual-para-a-criacao-de-aplicativos-de-leitura). Há intenção do projeto continuar em 2016 nesses moldes, agora com foco na qualidade da amostra. É crédito do Você Fiscal demonstrar a clara demanda por mecanismos de fiscalização das eleições por parte da sociedade.

O TSE também realizou a terceira edição dos Testes Públicos de Segurança (TPS) do Sistema Eletrônico de Votação entre os dias 08 e 10 de Março. Estive presente como observador externo indicado pela Sociedade Brasileira de Computação na Comissão Avaliadora e farei uma atualização mais detalhada quando toda a documentação se tornar pública no [site do evento](www.tse.jus.br/hotSites/testes-publicos-seguranca-2016/), respeitando o protocolo.

## Progresso

A auditoria solicitada pelo PSDB no final de 2014 já foi finalizada e o relatório pode ser encontrado na página do [Fórum do Voto Eletrônico](http://www.brunazo.eng.br/voto-e/), junto com um artigo mais curto publicado no [II Workshop de Tecnologia Eleitoral](http://sbseg2015.univali.br/anais/wte.html). A auditoria considerou uma base menor, porém melhor distribuída, e não encontrou divergências (página 138 do relatório). Os resultados parciais do nosso projeto colaboraram indiretamente com a auditoria.

O processamento continua em ritmo vagaroso. Relembrando:

* A base do 2o Turno enviada pelo aplicativo está completamente finalizada (7.020 BUs) e não foram encontradas divergências;
* A base do 1o Turno enviada pelo aplicativo foi pré-processada (7.641 BUs), mas a quantidade de fotos ainda impossibilita uma verificação manual: há seções eleitorais individuais com mais de 50 fotos;
* Abase do 2o Turno enviada pelo site do projeto (outros 7.200 BUs) impõe dificuldades pela heterogeneidade (fotos com diferentes resoluções, tamanhos, fundos, orientações, etc): nosso código para pré-processamento que confirmou origem de 87.1% dos BUs submetidos pelo aplicativo agora tem acurácia de apenas 12.4%, mesmo após ajustes. Do ponto de vista estatístico, essa última base possui viés e concentração parecidas com a base enviada pelo aplicativo, então o problema de qualidade da amostra ainda persiste.

Considerando toda a informação acima, entendemos ser mais interessante dedicar o tempo disponível ao planejamento da fiscalização das eleições de 2016, pois qualquer técnica desenvolvida perderá utilidade com a introdução dos códigos QR nos Boletins de Urna. Aproveito a oportunidade para agradecer novamente pelo apoio, doações, participação e engajamento da nossa comunidade!

Abraços,<br />
Diego Aranha

## Veja também:

[Resultado da conferência coletiva dos Boletins de Urna do 2º Turno](http://www.vocefiscal.org/blog/resultados-da-conferencia-coletiva-dos-boletins-de-urna/)
