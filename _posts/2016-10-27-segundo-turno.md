---
layout: post
title: Resultados da fiscalização
tags:
- "boletim-de-urna"
tagline: Resultados da fiscalização do primeiro turno das eleições municipais de 2016!
published: true
---

Olá!

Conseguimos terminar a fiscalização dos códigos QR recebidos da equipe do aplicativo Apura Fácil no primeiro turno! :)

Recebemos um total de 11460 códigos QR, contendo 5813 Boletins de Urna (BU) completos com assinaturas digitais válidas. Conseguimos extrair 306717 resultados desses códigos, devidamente verificados com a [base de BUs](www.tse.jus.br/eleicoes/estatisticas/repositorio-de-dados-eleitorais) publicada pelo TSE. A base recebida em 2016 corresponde a aproximadamente 72.5% da base do segundo turno de 2014 verificada pelo projeto.

A única divergência observada foi encontrada na zona 1 e seção eleitoral 813 da cidade de Manaus. A única hipótese plausível que encontramos para explicar o fenômeno é a cerimônia da
 [Votação Paralela](www.tre-am.jus.br/imprensa/noticias-tre-am/2016/Agosto/votacao-paralela-saiba-como-funciona):

* O código QR recebido possui um identificador de urna eletrônica diferente do divulgado no BU oficial.

* [As bases de correspondências esperadas e efetivadas](www.tse.jus.br/eleicoes/estatisticas/repositorio-de-dados-eleitorais) publicadas pelo TSE mostram que 3 urnas em AM foram instaladas na véspera das eleições, incluindo o identificador divulgado no BU oficial. Esse é o tamanho típico da amostra da Votação Paralela.

* A combinação de zona e seção foi noticiada pela imprensa local como [participante da Votação Paralela](http://new.d24am.com/noticias/amazonas/votacao-paralela-testar-confiabilidade-urnas-eletronicas/158685).

Alguém parece ter capturado o código da urna no final da Votação Paralela, talvez por ingenuidade ou para nos confundir? Geralmente fazem parte desta votação fiscais de partido, representantes da OAB/Ministério Público e técnicos da Justiça Eleitoral.
Ressaltamos que a amostra processada não é necessariamente representativa do total, de forma que só podemos atestar a transmissão correta dos resultados dessas seções eleitorais. Por fim, vale sempre lembrar que nossa fiscalização se restringe à transmissão dos resultados, pois o software de votação instalado nas urnas continua inauditável, para todos os propósitos.

Nossos scripts, programas e bases [estão publicados](https://github.com/vocefiscal/vocefiscal-qrcode).

Integram a equipe desta edição do projeto os alunos Ivan Petrin e Luiz Nachtigall do Instituto de Computação da UNICAMP. Obrigado pela colaboração!

Abraços,<br />
Diego Aranha
