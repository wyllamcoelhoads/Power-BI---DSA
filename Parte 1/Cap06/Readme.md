# Iniciando o capitulo 06 

## Área de recursos Humanos

O RH tem como função principal o ferenciamento e administração das atividades relacionadas ao pessoal de uma empresa, a fim de promover o desenvolvimento e a satisfação dos funcionários e, consequentimente, contribuir para o sucesso da organização!

Algumas das responsabilidades comuns do RH incluem:

* Recrutamento e seleção: publicar vagas, conduzir entrevistas, aplicar testes e avaliar canditatos para preenchimento das vagas da empresa.

* Treinamento e desenvolvimento: identificar as necessiadades de treinamentos dos funcionários, planejar e implementar programas de treinamento para melhorar habilidades e desenvolvimento profissional.

* Remuneração e beneficios: determinar salários competitivos e administrar programas de beneficios, como segura de saúde e ferias remuneradas.

* Gestão de conflitos: ajudar a resolver disputas entre funcionarios ou entre funcionarios e gestores, a fim de manter um ambiente de trabalho saudável e produtivo.

* Politicas de práticas de RH: desenvolver e implementar politicas e praticas de RH, como politicas de igualdade de oportunidades, diversidade e inclusão, e garantir que sejam aplicadas de maneira consistente.

* Avaliação do desempenho: avaliar regularmente o desempenho dos funcionarios, fornecer feedback e ajudar a definir metas e objetivos de desenvolvimento profissional.

Estas são apenas algumas das atribuições do RH que podem ser bastantes beneficiadas pela analise de dados!!!


## Quais são os principais Kpis da area de RH.

* Taxa de rotatividade: mede a frequencia que os funcionarios estão deixando a empresa.
* Satisfação do funcionario: mede o grau de satisfação dos funcionarios com relação ou trabalho, remuneração, ambiente de trabalho e oportunidades de desenvolvimento.
* Tempo médio para preenchimento de vagas: mede o tempo necessario para preencher uma vaga em aberto.
* Custo de contratação por funcionario: mede o custo total de contratar um novo funcionario, gastos como anucio de vagas, entrevistas, testes e treinamento.
* Participação em treinamento: mede o número de funcionarios que participam de programas de treinamento e desenvolvimento, que pode indicar o interesse em melhorar suas habilidades na carreira.
* Avaliação de desempelho: mede a avaliação do funcionario em um clico de trabalho.
* Nivel de absenteísmo: mede a frequencia com que os funcionarios faltam ao trabalho.
* NIvel de engajamento: escala que define quão engajado os funcionarios estão, normalmente medida em base no nivel de absenteísmo.


>[!NOTE]
>
> Cada empresa tem objetivos e necessidades diferentes, esses KPIS são exemplos porém é importente analisar e 
> observar quais podem ser importantes para retirarmos analises que fazam sentido para cada ambiente 

## O objetivo deste capitulo.

Neste capitulo vou desenvolver novas funções do power bi para apresentar analises relacionadas a área de RH, o intuito do trabalho é responder as seguintes perguntas;

1. Qual o total de funcionarios atualmente na empresa?
1. Qual o tempo médio de experiência dos funcionarios (em anos)?
1. Qual o total e percentual de funcionarios do gênero masculino e femenino?
1. Qual a média salarial mensal?
1. Qual o total de funcionarios por função?
1. Qual o percentual de funcionarios disponiveis para fazer horas extras?
1. Qual o nível de envolvimento dos funcionários no trabalho considerando 4 categoirias: Rim, Baixo, Medio e Alto?
1. Este item não deve estar no DashBoard, mais precisa ser calculado: Qual o total e o percentual de funcionarios que devem receber promoção? usando (anos de trabalho) usando a regra: Se o funcionario tiver 5 anos ou mais desde a ultima promoção, deve ter a promoção considerada. Caso contrario, a promoção não deve ser considerada.


> Este é um exemplo proposto da forma que as informações deveram ser apresentadas!

![modelo](/Parte%201/Cap06/imagem/MP3.png)


# Desenvolvendo o DashBoard

1. Qual o total de funcionarios atualmente na empresa?

> [!NOTE]  
>
>
> Usei o ID_funcionario, alterei o nome da variavel no campos do relatorio cartão, conforme abaixo!
> A informaçõa deve ser classificada como Contagem apenas, distinta ela conta os valores do id e não 
> apenas os registros.

![Total_Funcionarios](/Parte%201/Cap06/imagem/Total_Funcionarios.png)

1. Qual o tempo médio de experiência dos funcionarios (em anos)?

> [!NOTE]  
>
>
> Usei o Anos_experiencia, Um cartão como grafico, como é apenas uma informação então é o suficiente  
> resolve o problema, na imagem o valor de experiencia em anos foi de 11, porém na verdade a media do valor 
> das experiência em relação a todos os funcionarios, deu um valor de 11.29 alterei no caminho Formatar seu  
> visual.

![Experiencia](/Parte%201/Cap06/imagem/Experiencia_anos.png)


> Como foi formatado para aparecer zero casas decimais do valor do balão.

![formatacao](/Parte%201/Cap06/imagem/casasdecimais.png)

1. Qual o total e percentual de funcionarios do gênero masculino e femenino?

> [!NOTE]  
>
> Usei o Genero para contar os funcionarios e consigo filtrar o genero por masculino e feminino,   
> colocando o campo em contagem podemos marcar o genero escolhido em cada cartão, conforme as imagens  

![Imagem_masculino](/Parte%201/Cap06/imagem/masculino.png)

![Imagem_feminino](/Parte%201/Cap06/imagem/femenino.png)

> [!TIP]
>
> Não existe apenas uma forma de processar e apresentar os dados no power bi, na verdade seguindo a regra
> universal, nada é feito apenas de uma unica forma, problemas tem diversas soluções e podemos encontralas.

## Usando as medidadas em tabelas personalizadas

No power bi podemos processar os dados de forma que possamos deixar todo o trabalho mais facil, como precisamos facilidar trabalhos complexos, podemos dividir o trabalho em sub trabalhos assim será mais facil quando tivermos coisas mais complexas para fazer.

* Exemplo:

Preciso calcular a porcentagem dos funcionarios masculinos e femininos conforme imagem acima!

Porém para fazer isso de uma só fez o processo se torma muito complexo e eu foi acabar não prevendo o que o power bi ira fazer em casos como ZERO ou NEGATIVO na hora da divição, se estiver pensando em parte/todo"

Assim posso realizar medidas que irão faciliar as coisas!

![Nova_tabela](/Parte%201/Cap06/imagem/Nova_tabela.png)

Neste caminho podemos criar uma nova tabela que será usada para adicionar medidas novas(calculos para geração de novos dados com DAX)

![Total_func](/Parte%201/Cap06/imagem/Total_func.png)


Agora podemos usar essa tabela em outros problemas mais complexos, como realizar o calculo de porcentagem!


![Porcentagens](/Parte%201/Cap06/imagem/percentetotal.png)

Como podemos ver acima as informações de porcentagens foram apresentadas, usando o seguinte codido DAX.

`percentefeminino = medida[totalfuncionario],medida[totalfeminio],0`

Assim podemos usar as outras medidas já criadas para calcular novas medidas!

![percentefemenino](/Parte%201/Cap06/imagem/percentefemenino.png)


![percentemasculino](/Parte%201/Cap06/imagem/percentemasculino.png)

`percentemasculino = medida[totalfuncionario],medida[totalmasculino],0`

Esta é uma das vantagens, outra muito importante é que assim o power bi não precisa realizar calculos e recursos desnecessarios em tempo de execução já que a função já esta pre definida em uma nova medida!



