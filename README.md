 Contextualizando: 👾 <br>

A Resilia está pensando em lançar um novo sistema de acompanhamento e para isso precisa de ajuda para modelar um banco de dados que vai armazenar seus cursos, turmas e alunos.

✔ O que é para ser desenvolvido? <br>
Para apoiar nesse sistema recebemos a tarefa de realizar essa modelagem e responder algumas perguntas com nosso modelo:<br>
- Existem outras entidades além dessas três?<br>
- Quais são os principais campos e tipos?<br>
- Como essas entidades estão relacionadas?<br>

📊 Abaixo apresento a imagem da modelagem:<br>

<div align="center">
  <img width="80%" src="https://github.com/daiane1995/Projeto-Ind--M-4/files/10713784/My.First.Board.1.pdf" />
</div>

Explicação para cada atributo de cada entidade.<br>

Três entidades a mais (Unidades,Instrutor e Endereços), com essas entidades a mais podemos ter uma noção melhor, como?<br>

-Unidades: A entidade Unidades abrange todo o "universo" de todas as entidades, pois ela é mais importante, ela diz onde a instituição fica alocada mostrando com as colunas id (para pegar toda a linha), nome, bairro, estado cnpj e o tipo, a coluna tipo é para dizer se é a empresa Matriz ou Filial. <br>

-Cursos: A entidade Cursos abrange todos os cursos de todas as Unidades, ela recebe duas chaves estrageiras para saber em qual nome da unidade e o Estado da Unidade que fica alocada.<br>

-Alunos: A entidade Alunos é a base para o cadastro básico do aluno com as colunas nome, nascimento, cpf e recebendo duas chaves estrangeira "nome_cursos" para saber de qual curso o aluno pertence e "nome_unidades" para saber em qual unidade o aluno X pertence, essa chave estrangeira de Unidades é ideal para responder uma pergunta "Quantos alunos tem na Unidade X?".<br>

-Instrutor: A entidade Professor é basicamente a mesma de Alunos, sendo que acrescentei a especialidade do professor, a formação dele se é Frontend, Backend ou Full-Stack.<br>

-Endereços: Uma unidade muito importante é a endereço, pois ela pega todo o endereço de Alunos e Professores recebendo as colunas id, nome_professor, nome_aluno, rua, bairro, cidade, estado e cep. Repare que coloquei nome_professor e nome_aluno, quando utilizarmos o comando SELECT, utilizamos um ou outro, pois não seria possível utilizar as duas chaves e dando conflito, chamando a entidade nome_professor iria buscar pelo nome dele e aparecer todos os dados do mesmo.<br>

-Turmas: E por último a entidade Turmas, essa entidade é responsável por gerenciar as colunas id, nome, turno, alunosQuant, nome-cursos, modalidade_cursos e diasDasAulas_cursos, com essa entidade é possível saber a quantidade de alunos na turma X, e recebe três chaves estrangeira para saber qual curso é a turma X, quais são os dias de aulas e a modalidade do curso se é Presencial ou Ensino a Distância (EAD).<br>

🗝 Por que algumas entidades estão relacionadas uma com as outras (FK, chave estrangeira)?<br>🗝

Para o nosso banco de dados é fundamental ter elas, pois o relacionamento conseguimos responder algumas perguntas básicas, por exemplo:<br>
Quantos cursos X tem na unidade Y?
Quais são os cursos que tem na unidade Y?
Quantos alunos matriculados tem na unidade Y?
Quantos alunos tem em sala de aula do curso X?

Essas são algumas perguntas que poderiamos responder fácil com o banco de dados, pois elas estão relacionadas. Caso não conseguíssemos resolver alguma outra pergunta futuramente, poderíamos acrescentar uma FK em uma entidade para solucionar o problema ou dependendo da situação, acrescentar um atributo nas entidades.<br>

☑ Respostas das perguntas: ☑ <br>
⇨ Existem outras entidades além dessas três?
Sim, existem mais duas entidades, "Unidades" e "Professor".
Precisei colocar essas entidades para ter um parâmetro, aonde a entidade "Curso" fica vinculado a entidade "Unidades" e a entidade "Professor" fica vinculado a "Turmas", portanto, todas conectadas para um gerenciamento melhor no banco de dados.


⇨ Quais são os principais campos e tipos? <br>
Os principais campos são o nome, CPF, nascimento, RG e sem dúvida o ID referenciando toda a entrada na Entidade.
Os dois tipos mais importante são a Chave Primária e a Chave estrangeira.


⇨ Como essas entidades estão relacionadas? <br>
As entidades estão relacionadas com as chaves estrageiras (FK), como podemos ver na imagem feita no Miro , em algumas entidades tem um atributo com "id_nomeDaEntidade", fazendo com que elas fiquem relacionadas.<br>

Ferramentas utilizadas nesse projeto:💻<br>
 Miro.com;<br>
 VS Code.
