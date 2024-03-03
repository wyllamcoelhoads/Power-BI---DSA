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
> Usei o ID_funcionario, alterei o nome da variavel no campos do relatorio cartão, conforme abaixo!
>[!NOTE] A informaçõa deve ser classificada como Contagem apenas, distinta ela conta os valores do id e não 
> apenas os registros.

![Total_Funcionarios](/Parte%201/Cap06/imagem/Total_Funcionarios.png)
