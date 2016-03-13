---
layout: post
title: Boletim de Notícias
tags:
- "boletim-de-urna"
tagline: Faz muito tempo desde a última atualização, então resolvi fazer um apanhado do que aconteceu desde então!
published: true
---

- O Você Fiscal foi premiado em Novembro do ano passado pela edição brasileira da revista MIT Technology Review. O prêmio se chama Inovadores Menores de 35 anos Brasil e participar do evento foi muito interessante para estabelecer colaborações e discutir idéias para a evolução do projeto;
- O voto impresso foi aprovado para reintrodução nas eleições de 2018, após longa tramitação (http://www12.senado.leg.br/…/eleicoes-terao-voto-impresso-a…). Um dos pontos negativos do Projeto de Lei aprovado é a ausência de fases de auditoria e recontagem, que poderiam ter sido especificadas. Estamos nos aproximando de pesquisadores internacionais para estudar procedimentos que facilitem a adoção do recurso nas eleições brasileiras;
- O TSE anunciou poucos dias após nossa última atualização a introdução de um código QR com assinatura digital nos Boletins de Urna das próximas eleições. Esse recurso deve facilitar em muito a aquisição de dados, pois toda a dificuldade com extração de informação via reconhecimento de caracteres torna-se trivial. O manual com a especificação já foi publicado (http://www.tse.jus.br/…/qr-code-no-boletim-de-urna-manual-p…). Há intenção do projeto continuar em 2016 nesses moldes, agora com foco na qualidade da amostra. É crédito do Você Fiscal demonstrar a clara demanda por mecanismos de fiscalização das eleições por parte da sociedade;
- O TSE realizou a terceira edição dos Testes Públicos de Segurança do Sistema Eletrônico de Votação entre os dias 08 e 10 de Março. Estive presente como observador externo indicado pela Sociedade Brasileira de Computação na Comissão Avaliadora e farei uma atualização mais detalhada quando toda a documentação se tornar pública no site do evento, respeitando o protocolo;
- A auditoria solicitada por partido político no final de 2014 já foi finalizada e o relatório pode ser encontrado na página do Fórum do Voto Eletrônico (http://www.brunazo.eng.br/voto-e/), junto com um artigo mais curto publicado no II Workshop de Tecnologia Eleitoral. A auditoria considerou uma base menor, porém melhor distribuída, e não encontrou divergências (página 138 do relatório). Os resultados parciais do nosso projeto colaboraram indiretamente com a auditoria;
- O processamento continua em ritmo vagaroso. Relembrando: a base do 2o Turno enviada pelo aplicativo está completamente finalizada (7.020 BUs) e não foram encontradas divergências; a base do 1o Turno enviada pelo aplicativo foi pré-processada (7.641 BUs), mas a quantidade de fotos ainda impossibilita uma verificação manual: há seções eleitorais individuais com mais de 50 fotos; a base do 2o Turno enviada pelo site do projeto (outros 7.200 BUs) impõe dificuldades pela heterogeneidade (fotos com diferentes resoluções, tamanhos, fundos, orientações, etc): nosso código para pré-processamento que confirmou origem de 87.1% dos BUs submetidos pelo aplicativo agora tem acurácia de apenas 12.4%, mesmo após ajustes. Do ponto de vista estatístico, essa última base possui viés e concentração parecidas com a base enviada pelo aplicativo, então o problema de qualidade da amostra ainda persiste.
Considerando toda a informação acima, entendemos ser mais prudente interessante o tempo disponível ao planejamento da fiscalização das eleições de 2016, pois qualquer técnica desenvolvida perderá utilidade com a introdução dos códigos QR nos Boletins de Urna. Aproveito a oportunidade para agradecer novamente pelo apoio, doações, participação e engajamento da nossa comunidade!
Abraços,
Diego Aranha

## Conferência coletiva

Conforme publicado anteriormente, os Boletins de Urna submetidos pelo aplicativo Você Fiscal foram processados por análise automática utilizando reconhecimento de caracteres,
que permitiu a inspeção e correção de inúmeros erros de preenchimento.

Na ocasião, a extração automática de mais de 20 mil pares de candidato/votação dos Boletins de Urna permitiu conferência com os resultados eletrônicos publicados pelo TSE, onde foi encontrada discrepância em aproximadamente 20% dos pares extraídos. Por uma questão de transparência, resolvemos distribuir o esforço de verificação entre a comunidade, para que as discrepâncias fossem resolvidas coletivamente.

## Resultados parciais

Foram recebidos pelo aplicativo Você Fiscal 8.824 conjuntos de fotos referentes ao Segundo Turno das eleições. Eliminando fotos marcadas como inviáveis e seções duplicadas, foram verificadas 7.020 seções eleitorais por conferência manual coletiva, correspondentes a 1.6% das urnas eletrônicas do país e 4.1% dos eleitores (ou 4.644.385 de votos).

Até então, já foram realizadas mais de 25800 conferências, na direção de atingir pelo menos 3 conferências distintas por cada Boletim de Urna submetido. Após a conferência
manual coletiva, [persistiram 143 Boletins de Urna como divergentes](http://somos.vocefiscal.org/relatorios/bus-marcados-para-revisao/). Nova análise manual desses 143 Boletins de Urna por parte da equipe não apresentou nenhuma discrepância em relação aos resultados publicados pelo TSE. Em alguns poucos casos, a conferência detectou que fotos de [Zerésima](http://somos.vocefiscal.org/relatorios/bus-marcados-para-revisao/13) ou [BUs de Primeiro Turno](http://somos.vocefiscal.org/relatorios/bus-marcados-para-revisao/35) haviam sido submetidas como de Segundo Turno. Vale lembrar que o Você Fiscal analisa apenas a transmissão dos resultados parciais de eleição, não se manifestando sobre qualquer outro componente do sistema de votação eletrônica utilizado em 2014, por simples falta de acesso.

## Novidades

Desde nossa última comunicação, várias coisas importantes aconteceram:

* Um projeto de pesquisa foi submetido para iniciativa de dados abertos da Microsoft. A aprovação do projeto nos concedeu uma bolsa de Iniciação Científica ou Mestrado para que um aluno trabalhe em tempo integral no aprimoramento das técnicas automáticas de reconhecimento de caracteres. Esse passo é fundamental para se explorar o restante da base de dados: as fotos de BUs do Segundo Turno são substancialmente maiores e menos padronizadas, exigindo esforço maior de pré-processamento; as fotos de BUs do Primeiro Turno são muito numerosas devido ao tamanho dos documentos, inviabilizando a conferência manual. A princípio, contar com uma base já validada manualmente de fotos de tamanho expressivo permitirá que o treinamento e ajuste do reconhecimento de caracteres seja mais preciso.

* Estamos trabalhando há meses com uma equipe reduzida, pois os recursos do projeto foram esgotados ainda em 2014. Nossa [prestação de contas](https://docs.google.com/spreadsheets/d/1w1Hv3CuB4ziF3aTNP7zK9RVrWCqfBZAGv8IwoZYJoI4/pubhtml) já está disponível há alguns dias no site do projeto. Incluímos apenas os custos previstos na campanha de financiamento coletivo, e foram ignorados alguns custos posteriores com armazenamento de dados em nuvem e reenvio de recompensas financiados com recursos próprios.

* Estamos produzindo um artigo científico detalhando a experiência, suas limitações e resultados parciais. No mesmo artigo, é proposto um mecanismo simples de código de barras para facilitar a verificação de Boletins de Urna com um dispositivo móvel, idéia que surgiu após várias iterações com membros da comunidade. Os resultados desse trabalho deverão ser apresentados na II edição do Workshop de Tecnologia Eleitoral, evento satélite do [XV Simpósio Brasileiro em Segurança da Informação e de Sistemas Computacionais](http://sbseg2015.univali.br/). 

Apesar da demora e dificuldades na condução do trabalho, esse projeto já é o maior esforço coletivo para auditoria de resultados eleitorais conduzido no mundo! Parabéns e obrigado, não teríamos chegado até aqui sem a colaboração de todos.

Ainda há muito trabalho para que a idéia evolua e se torne mais simples, descentralizada e eficaz, mas acreditamos ter feito progresso importante nessa área e contribuído significativamente para a reinstalação do debate sobre a segurança e a transparência do sistema eletrônico de votação no Brasil.

Abraços,<br />
Diego Aranha

## Veja também:

[Resultado da conferência coletiva dos Boletins de Urna do 2º Turno](http://www.vocefiscal.org/blog/resultados-da-conferencia-coletiva-dos-boletins-de-urna/)
