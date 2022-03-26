# Programação  Orientada por Objetos  2021/2022

## Ficha de Laboratório ==#4==

> ## Objetivos
> 
> - Introdução ao desenho de aplicações. 
>   Pretende-se dar início à etapa de desenho de uma aplicação, trabalhando apenas um subconjunto do Projeto I.

## Trabalho a entregar:

- Ficheiro de texto com:
  - a análise substantivo/verbo;
  - as cartas CRC.
- O esboço das classes envolvidas nas cartas CRC.

## Descrição do Problema

O objetivo do Projeto I passa pelo desenvolvimento de uma solução para gerir os resultados de processos eleitorais em Portugal.  Existem basicamente quatro (4)  tipos de eleições em Portugal:  Presidenciais, Legislativas, Europeias e Autárquicas. Cada uma delas tem especificidades que a distingue das demais . Contudo, excetuando as eleições presidenciais, em que o voto é efetuado numa pessoa especifica, todas as outras têm como base o cálculo de mandatos a atribuir a cada partido, tendo em conta o  [Método de Hondt]([Método de Hondt | Comissão Nacional de Eleições](https://www.cne.pt/content/metodo-de-hondt)).

### O Processo Eleitoral

O processo eleitoral desenrola-se em mesas de votos que estão associadas a freguesias. As freguesias estão associadas a concelhos que por sua vez estão associados a distritos.

De acordo com os cadernos eleitorais cada votante tem associada uma mesa especifica e apenas pode exercer o voto nessa mesa, indicando para isso o seu número de eleitor ou cartão de cidadão. Naturalmente só pode votar uma vez.

São ainda admissíveis votos antecipados e votos efetuados por cidadãos portugueses que se encontrem no estrangeiro.

Nos casos dos votos antecipados, os votos são enviados fisicamente para as mesas de votos respetivas onde é registada a data do voto do cidadão e colocado na urna de voto o voto efetuado pelo eleitor.

Os votos são efetuados num boletim de voto fornecido pela mesa ao eleitor no momento da votação.

Todas as eleições se processam durante um determinado período horário. As urnas devem abrir às 8h e encerrar às 19h.

**Votos**

Um voto pode ser considerado: 

- **Válido** – quando é selecionada corretamente uma das opções disponíveis;
- **Branco** - quando não é selecionada nenhuma opção e o boletim de voto fica intacto;
- **Nulo** –  quando é rasurado ou não é clara a opção de votação do eleitor.

Nota: votos brancos e votos nulos não são considerados votos válidos.

**Eleições Presidenciais**

Nas eleições presidenciais vota-se para a eleição do presidente da república. É eleito Presidente da República o cidadão Português que se apresente a eleições, com mais de 35 anos e que obtenha pelo menos 50% dos votos.

Caso nenhum dos candidatos obtenha 50% dos votos (ou em caso de haver 2 candidatos empatados, cada um, com 50% dos votos), haverá um segundo sufrágio (segunda volta), ao qual concorrerão apenas os dois candidatos mais votados (que não tenham retirado a sua candidatura).

**Eleições Legislativas**

Nas eleições legislativas vota-se para a constituição do Parlamento português. Este é constituído por uma câmara de Deputados única designada Assembleia da República. É um dos dois órgãos de soberania eletivos previstos na Constituição, além do Presidente da República, cabendo-lhe o papel constitucional de "assembleia representativa de todos os cidadãos portugueses”.

A definição dos mandatos é atribuída de acordo com o método de *Hondt*   e estes são definidos ao nível dos distritos. Ou seja, no conjunto de 230 deputados eleitos,   cada distrito elege um número predeterminado de acordo com a sua densidade populacional.

**Eleições Europeias**

Nas eleições europeias vota-se para o parlamento europeu. Neste caso o número de mandatos a
atribuir é ao nível nacional.

**Eleições Autárquicas**

O processo eleitoral autárquico consiste em 3 processos eleitorais em simultâneo:

- Câmara Municipal;
- Assembléia Municipal;
- Assembléias de Freguesia .

### Principais Funcionalidades envolvidas no Processo Eleitoral

Como já informado, existem quatro (4) tipos de eleições que possuem configurações e comportamentos distintos. 
Assim, a aplicação a desenvolver deverá permitir:

A aplicação a desenvolver deverá permitir:

- A criação de um processo eleitoral, para cada tipo de eleição, com as respetivas configurações (Período eleitoral, Candidatos, Distritos, Concelhos, Freguesias, Mesas…)

- Configuração dos boletins de voto por processo eleitoral

- Indicação do número de votantes por mesa

- O carregamento dos votos em cada uma das mesas

- Apresentação dos resultados eleitorais:
  
  + Número de freguesias apuradas versus o total de freguesias existentes;
  + Taxa de abstenção;
  + Número de votos: válidos, brancos e nulos com a respetiva percentagem;
  + Número de mandatos atribuídos, número total de votos e % de votos.

- Deverá ser possível carregar através de ficheiro a estrutura de distritos, concelhos, freguesias e mesas (ficheiro fornecido em anexo ao enunciado)

- Em qualquer fase de carregamento dos votos deve ser possível guardar e ler o progresso de carregamento da informação.

## Implementação

### Nível 1:

- Copie o conteúdo dos tópicos **Processo Eleitoral e Principais Funcionalidades**   para um processador de texto à sua escolha.
- No texto copiado, pinte de verde todos os substantivos (nomes) para começar a ter uma ideia das entidades envolvidas no problema.
- Pinte de vermelho todos os verbos para começar a ter uma ideia das ações envolvidas no projeto.

### Nível 2:

- Copie todos os substantivos para uma lista e elimine os duplicados. 
- Copie todos os verbos e respetivos substantivos associados para outra lista e elimine as ações repetidas.  

### Nível 3:

- Com base nos substantivos extraídos, faça uma 3ª lista em que identifica o que lhe pareça poder vir a constituir classes de objetos.
- Para cada uma delas faça a respetiva carta CRC, tendo em conta **apenas** a informação disponível na descrição do Processo Eleitoral   Deve ter presente o princípio da responsabilidade única.

### Nível 4:

- Com base nas cartas CRC das classes identificadas no Nível 3 defina uma primeira aproximação da interface das classes envolvidas (métodos públicos) . Crie um esboço da implementação da classe, com a sua estrutura, os cabeçalhos dos métodos públicos, ainda sem o código interno, e a respetiva documentação destes métodos.

### Nível 5:

- Crie um esboço da implementação das funcionalidades principais identificadas na classe dos votantes, com a estrutura da classe, os cabeçalhos do métodos públicos, ainda sem o código interno, e a respetiva documentação destes métodos.

==**Notas**==:

Para os identificadores siga as convenções adotadas normalmente, em particular:

1. A notação **camelCase** para o nome das variáveis locais e identificadores de atributos e métodos.

2. A notação **PascalCase** para os nomes das classes.

3. Não utilize o símbolo ‘_’, nem abreviaturas nos identificadores.
