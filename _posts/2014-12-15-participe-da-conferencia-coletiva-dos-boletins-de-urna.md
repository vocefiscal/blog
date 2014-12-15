---
layout: post
title: Resultado da análise automática do 2º turno e início da conferência coletiva
tags:
- "boletim-de-urna"
tagline: 20% dos resultados da análise automática divergiram dos valores oficiais. Começa hoje o mutirão para conferi-los manualmente.
published: true
---

<a href="http://somos.vocefiscal.org/conferir" target="_blank">
  ![](http://www.vocefiscal.org/blog/assets/images/conferencia-coletiva.png)
</a>

## Análise automática das imagens

A análise foi feita até agora com as imagens enviadas pelo aplicativo Você Fiscal. As fotos enviadas pelo site já estão em pré-processamento.

O primeiro passo da análise automática foi a triagem, com o objetivo de confirmar a origem (zona, zeção, município e Estado) dos Boletins de Urna. Para tanto, utilizamos reconhecimento de caracteres treinado especificamente com a fonte da Urna Eletrônica para detectar o "número de correspondência" de cada Boletim de Urna fotografado e, utilizando [base de correspondências efetivadas do TSE](http://www.tse.jus.br/eleicoes/estatisticas/repositorio-de-dados-eleitorais), verificar se as informações preenchidas pelo usuário eram compatíveis. Em caso negativo, a intervenção manual permitiu corrigir as informações e anotar o Boletim de Urna corretamente. Caso mesmo a inspeção manual não tenha sido suficiente para confirmar a origem ou caso as fotos não fossem de um Boletim de Urna, a submissão não fez parte da análise.

Em seguida, utilizamos técnicas simples de processamento de imagem (binarização) para aumentar o contraste das imagens nas fotos de Boletins de Urna cuja origem foi confirmada. O reconhecimento de caracteres posterior permitiu extrair as informações das fotos e conferi-las com as disponibilizadas pelo TSE no [repositório de dados eleitorais](http://www.tse.jus.br/eleicoes/estatisticas/repositorio-de-dados-eleitorais). Essa extração permitiu extrair até agora mais de 20 mil pares de candidato e votação, dos quais aproximadamente 20% não foram compatíveis com a informação do TSE. Resta saber se por erro no reconhecimento de caracteres (mais provável) ou erro/fraude nas eleições.

Para finalizar a tarefa de verificação das submissões do segunto turno, o trabalho restante será distribuído entre usuários voluntários da comunidade, de forma que cada Boletim de Urna será considerado validado após um número mínimo de verificações. Os Boletins de Urna que foram verificados por software também poderão ser verificados pela comunidade, mas contarão com aprovação parcial que acelerará a verificação distribuída.

## Participe da conferência coletiva

**Quem vota é quem conta.** Este é um princípio básico de transparência eleitoral e fiscalização cidadã que o Brasil não segue, mas que estamos juntos trabalhando para mudar. Novamente, precisamos da sua participação.

**Auditoria = registro + conferência**

No dia das eleições, milhares de cidadãos e cidadãs deram exemplo por todo o país, exigindo mais transparência no processo eleitoral e, através de ação direta, colocando a atuação do governo sob supervisão cidadã (como deveria ser, sempre). Nosso objetivo: **registrar evidências.**

Mais de 20 mil Boletins de Urna foram fotografados nesta mobilização histórica, mostrando mais uma vez que a sociedade civil é capaz de se organizar e trabalhar junto sim, independente de fronteiras partidárias e rivalidades ideológicas, tanto dentro quanto fora da Internet.

Registrar boletins de urna era possível mesmo antes da existência do projeto Você Fiscal e da publicação do nosso aplicativo. O que fizemos foi trazer o assunto ao debate público e **empoderar os eleitores com conhecimento e software** para desobstruir e amplificar a capacidade de fiscalização da própria sociedade. O que antes seria um esforço individual isolado pôde, pela primeira vez, contar com a força e o apoio mútuo de uma *comunidade* de cidadãos mobilizados.

---

Agora que temos o **registro**, precisamos fazer a **conferência**.

Com software, conseguimos fazer uma análise prévia automática, o que aumenta a confiança nos casos em que os números bateram. Mas software é passível de erro (senão não estaríamos exigindo registro impresso do voto), então mesmo os que bateram precisam ser revisados manualmente.

Além destes, porém, **em pelo menos 20% dos casos, o número extraído da foto via software não bateu com o resultado oficial do TSE**. Estes precisam ser checados com atenção redobrada.

Para que cada um dos BUs analisados seja conferido por pelo menos 3 pessoas diferentes, precisamos de 26.472 checagens. Somos uma equipe de duas pessoas e não conseguiríamos fazer isso sozinhos. Mas mesmo que conseguíssemos, por que alguém deveria confiar na nossa palavra?

A sociedade vota, a sociedade confere, certo? Para facilitar a conferência coletiva, fizemos uma ferramenta em software, assim como fizemos para facilitar o registro coletivo.

Em última instância, a decisão de ter eleições auditáveis e **auditadas** só pode ser tomada pelos próprios eleitores. Não substituímos o trabalho da sociedade, apenas a equipamos com ferramentas para que tenha maior impacto.

Cada espaço de atuação do governo iluminado por um olhar cidadão é um espaço a menos onde coisas podem ser feitas contra o nosso interesse. Vamos nos unir mais uma vez e manter essa luz acesa?

Por favor, participe clicando abaixo:

<p style="text-align: center;"><a href="http://somos.vocefiscal.org/conferir" target="_blank" class="btn btn-large btn-success">Participar da Conferência Coletiva</a></p>

Obrigado!

Abraços,<br />
Diego e Helder

## Dúvidas
Se tiver dúvidas sobre este artigo ou sobre como usar o site de conferência coletiva, por favor, deixe um comentário abaixo para que possamos atualizar este texto com a resposta. Se você souber a resposta de alguma pergunta feita por outra pessoa, por favor, colabore respondendo. Obrigado!

* Há relatos de usuários do Firefox que tiveram problemas com o site. Estamos investigando mas, enquanto isso, pedimos que usem o Google Chrome.

## Veja também:

[E se o Você Fiscal não encontrar nenhuma fraude?](http://www.vocefiscal.org/blog/e-se-o-voce-fiscal-nao-encontrar-nenhuma-fraude/)
