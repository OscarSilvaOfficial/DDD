# Leitura do livro DDD

## Descrição
Aqui coloco o resumo da minha leitura sobre o livro DDD. 
Com certeza o raciocínio e escrita etará bagunçado, mas esse repositório serve apenas para eu organizar o que entendi sobre o livro

## Resumo dos capítulos

### Prefácio

#### *O desafio da complexidade*
No capítulo é citado que, a grande complexidade do software moderno não está no avanço técnológico, mas sim na camada no negócio, por isso devemos focar a maior parte do esforço nisso.

``NOTA: Fico relutante nesse ponto, pois em alguns projetos em que trabalhei, essa não era a maior dificuldade, apesar de que sim, ela existia também.``

#### *Design x Processo de desenvolvimento*
No capítulo, o autor começa com uma crítica, pelo fato que o engenheiros normalmente não entendem o momento de brigar para estabelecer certos conceitos de design, ou abrir mão deles, dado ao contexto que estão vivendo

``NOTA: Realmente, isso é um problema na maioria dos desenvolvedores mais puristas.``

Além disso, é criticado as metodologias de engenharia de software antecessoras as metodologias ágeis. A prática do DDD é guiada a melhorias e refatorações contínuas, sem a necessidade de passar por grandes processos de iniciação da construção, como a grande quantidade de documentações, diagramações e etc. 

``NOTA: Me pergunto se isso realmente é possível, como planejar e entender os domínios sem processos iniciais de entendimento?! O que por consequência, deveria gerar um bom número de documentações, e provavelmente, sem nenhuma entrega por um determinado tempo. Além disso acho difícil no processo ágil ATUAL, priorizar refatorações para manter o design de software no lugar de uma nova feature.``

### Colocando o modelo de domínios em ação

#### *O coração do software*

Na concepção do autor, para construir software, é necessário entender do negócio em que está inserido, pois nele resida as maiores complexidades dentro de um sistema, portanto os desenvolvedores devem enteder muito bem se não for o negócio como um todo, pelo menos a parte em que está envolvido.

``NOTA: Isso realmente faz muito sentido, pensando em desenvolvedores mais experientes, que possam guiar os times tanto com a visão mais técnica, quanto com os conhecimentos de negócio, mas acho isso impraticável em ambientes sem equipes extremamente estruturadas.
Além disso, acredito que seria necessário um time com turnover baixíssimo, para que o conhecimento técnico e de negócio não se perca, ou um tempo bem dedicado a documentar esse processo de aprendizado do negócio.``

### Assimilando o conhecimento

O capítulo é iniciado com um caso de uso, onde o desenvolvedor precisou construir um software para PCI.
Para se comunicar com os engenheiros eletrônicos, o desenvolvedor precisou conversar com os engenheiros e entender profundamente o funcionamento da placa para logo em seguida, traduzir os comportamentos necessários para o software.

No processo de entendimento, ele utilizou diagramas e foi construindo seus modelos de dados.

Além disso, para conseguir se comunicar de forma assertiva, foi fundamental que eles conseguisem falar a mesma lingua, que no caso, seria entender o necessário sobre os componentes de hardware que envolvem a PCI
