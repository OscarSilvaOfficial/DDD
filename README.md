# Domain Driven Design - Resumo e Análise

![DDD image](./ddd.jpg)

## Descrição
Aqui coloco o resumo da minha leitura sobre o livro DDD.

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

***

### Colocando o modelo de domínios em ação

#### *O coração do software*
Na concepção do autor, para construir software, é necessário entender do negócio em que está inserido, pois nele resida as maiores complexidades dentro de um sistema, portanto os desenvolvedores devem enteder muito bem se não for o negócio como um todo, pelo menos a parte em que está envolvido.

``NOTA: Isso realmente faz muito sentido, pensando em desenvolvedores mais experientes, que possam guiar os times tanto com a visão mais técnica, quanto com os conhecimentos de negócio, mas acho isso impraticável em ambientes sem equipes extremamente estruturadas.
Além disso, acredito que seria necessário um time com turnover baixíssimo, para que o conhecimento técnico e de negócio não se perca, ou um tempo bem dedicado a documentar esse processo de aprendizado do negócio.``

***

### Assimilando o conhecimento

#### *Os ingredientes de uma modelagem eficaz*
O capítulo é iniciado com um caso de uso, onde o desenvolvedor precisou construir um software para PCI.
Para se comunicar com os engenheiros eletrônicos, o desenvolvedor precisou conversar com os engenheiros e entender profundamente o funcionamento da placa para logo em seguida, traduzir os comportamentos necessários para o software.

No processo de entendimento, ele utilizou diagramas e foi construindo seus modelos de dados.

Além disso, para conseguir se comunicar de forma assertiva, foi fundamental que eles conseguisem falar a mesma lingua, que no caso, seria entender o necessário sobre os componentes de hardware que envolvem a PCI


#### *Extraindo um conceito oculto*
O autor da um exemplo de domínio e explica que no momento da criação (ou modificação) do software, é ideal separar regras de negócio. Caso seja uma única regra que não possua variações, o simples ato de separar do resto do código, e nomea-la com a regra do domínio é extremamente importantre.

E em casos onde essa regra possua muitas variações, talvez seja mais interessante utilizar o `design pattern Strategy`.

#### *Comunicação e uso da linguagem*
Nesse capítulo é enfatizado a questão da liguagem e como usar nomes de negócios no planejamento da arquitetura (em diagramas, fluxogramas, e documentações em geral) e código pode fortalecer o conhecimento a respeitodas regras que envolvem o negócio, e mais importante ainda, diminuir os ruídos de comunicação entre negócio e desenvolvimento. Essa linguágem unificapa, chama-se **ubiquitous language**, ou *linguágem unipresente*.

``NOTA: Nas experiências que tive, um dos problemas que gerava mais confusão, relamente era a questão da comunicação e entendimento do negócio, então fazer o esforço de colocar a linguagem do negócio no código, para que no longo prazo o time esteja mais acostumado, realmente parece fazer muito sentido.``

#### *Documentos e diagramas*
Nessa sessão, o autor indica que usa diagramas para exemplificar o raciocínio. Normalmente usado de forma muito simples, para que seja fácil e rápido de entender.
A função de um diagrama é, comunicar bem a sua idéia, então se esse papel for cumprido, está de ótimo tamanho.

#### *Documentos de design escritos*
Documentação é extremamente importante para um projeto, mas ao mesmo tempo, extremamente desafiadora, principalemte pelo fato da manutenção do software torna-la fácilmente obsoleta.

O Autor explica que na metodologia agil *Extreme Programming*, documentações são descartáveis, mas autor contrapõe isso, pois acredita que documentações de alto nível de design são **extremamente** importantes para o entendimento como um todo.

#### *Modelos explanatórios*
Modelos explanatórios são representações simplificadas de um domínio que ajudam a esclarecer e comunicar aspectos complexos desse domínio de uma maneira mais fácil de entender. Eles não são apenas descrições detalhadas da realidade, mas são construídos para fornecer uma compreensão clara sobre o funcionamento de partes críticas de um sistema.

1 - *Exemplo descritivo de modelo explanatório*

```
Um exemplo de **modelo explanatório** no contexto do DDD poderia ser em um domínio de sistema bancário,
onde o objetivo é facilitar a comunicação entre desenvolvedores e especialistas no domínio (nesse caso, talvez gerentes de banco ou analistas financeiros).
Vamos imaginar uma funcionalidade de **transferência de dinheiro entre contas**.

### Exemplo:

Domínio: Sistema bancário

Modelo Explanatório: Transferência de Dinheiro

1. Entidade: Conta Bancária
   - Cada conta tem um saldo.
   - O saldo pode aumentar ou diminuir dependendo de transações.

2. Entidade: Cliente
   - Um cliente é o proprietário de uma ou mais contas bancárias.

3. Ação (Serviço): Transferir Dinheiro
   - Um cliente pode iniciar uma transferência de dinheiro de uma conta para outra.
   - Regras:
     - A conta de origem deve ter saldo suficiente.
     - Se a transferência for bem-sucedida, o saldo da conta de origem diminui e o da conta de destino aumenta.
     - A transação deve ser registrada no histórico da conta.
```

2 - *Exemplo através de uma imagem de modelo explanatório*

![image](https://github.com/user-attachments/assets/a67e4ac0-ebce-4f00-89af-cd226022a563)

#### *Paradigmas da modelagem e assistência as ferramentas*
O autor indica liguagens de programação que dão suporte a *orientação a objeto*
