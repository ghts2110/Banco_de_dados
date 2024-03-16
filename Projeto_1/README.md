# Banco_de_dados

Gabriel Henrique Torres
00000844543

Biblioteca

A entidade Cliente herda alguns atributos da entidade Pessoa, tais como sexo, e-mail e nome. Além disso, possui atributos próprios, como endereço, CPF (que é uma chave, assim como o atributo nome) e data de nascimento. O Cliente tem a capacidade de comprar ou solicitar empréstimos de materiais, tanto de leitura quanto de áudio, que serão mencionados em breve. Somente após a compra, o cliente poderá dar uma nota para o produto adquirido. Em contraste com a entidade anteriormente citada, o Cliente só possui relação de compra com os materiais de papelaria. Por fim, em relação à entidade Cliente, ele também tem uma relação na qual pode ser ajudado por um funcionário.

Referenciando a entidade Funcionário, assim como a entidade Cliente, esta também herda alguns atributos da entidade Pessoa. Além disso, possui atributos exclusivos, como a função do funcionário e seu salário. Observa-se que essa entidade possui uma relação consigo mesma, uma vez que um funcionário em um cargo de maior prioridade, como um gerente, pode gerenciar o trabalho dos outros. Além disso, como mencionado anteriormente, os funcionários têm a relação de ajudar os clientes.

Indo para a entidade Material de papelaria, observamos que ela possui os atributos de vencimento, preço e ID (como uma chave para diferenciar dos outros produtos). Os materiais de papelaria têm uma relação com a entidade Empresa, que contém o atributo nome como chave. Isso ocorre porque existe a possibilidade de um cliente querer ver as sugestões de produtos que uma empresa produz, sendo importante ter tanto o ID quanto o nome da empresa como uma chave.

Voltando à entidade citada, quando se trata da entidade Cliente, há a referência à entidade Material de leitura/escuta, que basicamente se refere a livros, e-books, audiobooks, revistas e ingressos. Esta entidade possui os atributos de lançamento, preço, e tanto ID quanto nome como chaves. Além disso, ela tem relação com as entidades Autor e Editora, que têm o nome como chave pelos mesmos motivos da entidade Empresa mencionada anteriormente. A entidade Autor, assim como Funcionários e Clientes, herda os atributos da entidade Pessoa, e além disso, tem uma relação de pagamento com a entidade Editora.

Como mencionado anteriormente, a entidade Revista é uma das opções disponíveis para escolha pelo cliente. A única diferença dessa entidade em relação às outras é o seu atributo de conteúdo, que indica o que está contido dentro daquela revista.

A entidade Ingresso possui o atributo quantidade para garantir que não será vendido mais ingressos do que a disponibilidade. Esses ingressos têm uma relação para fornecer entrada à entidade Evento, que contém o atributo tópico. Além disso, o evento tem uma relação de ser apresentado pela entidade Palestrante, que herda os atributos da entidade Pessoa.

Falando agora da entidade Livro, ela é uma entidade simples que não tem relação com nenhuma outra entidade. No entanto, possui o atributo número de cópias, pelo mesmo motivo presente na entidade Revista, assim como o atributo quantidade em Ingresso. Outros atributos da entidade Livro incluem o número de páginas e o gênero, que são sempre importantes em um banco de dados. Para finalizar, há o atributo tipo de capa, pois existem pessoas que preferem capas duras e outras que preferem capas moles, então é útil ter essa informação para atender às preferências dos clientes.

A última entidade dentro das possibilidades da entidade Material de leitura/escuta é a entidade Apps, com o atributo app para identificar exatamente em qual aplicativo a compra está sendo feita, e o atributo memória para informar quanto de espaço aquele e-book ou audiobook vai ocupar na memória. Essa entidade tem a mesma relação de disponibilizar tanto para a entidade E-book quanto para a entidade Audiobook, que possuem os atributos páginas e horas, respectivamente.

Referências entre entidades:

1 cliente compra 0/n materiais de papelaria
1 cliente compra 0/n materiais para ler ou escutar
1 cliente pede empréstimo de 0/n materiais para ler ou escutar
0/n clientes podem ser ajudados por 0/1 funcionários

0/n funcionários são gerenciados por 1/n funcionários
1/n funcionários gerenciam  0/n funcionários
0/1 funcionários ajudam 0/n clientes

0/n materiais de papelaria são comprados por 1 cliente
1/n materiais de papelaria são fabricados por 1/n empresas

1/n empresas fabricam 1/n materiais de papelaria

0/n materiais para ler ou escutar são comprados por  1 cliente
0/n materiais para ler ou escutar são dados como empréstimo para 1 cliente
1/n  materiais para ler ou escutar são escritos por 1/n autores
1/n  materiais para ler ou escutar são publicados por 1/n editoras
1/n autores escreve 1/n materiais para ler ou escutar
1/n autores são pagos por 1/n editoras

1/n editoras publicam 1/n materiais para ler ou escutar
1/n editoras  pagam 1/n autores

1 ingresso disponibiliza a entrada 1/n eventos

1/n eventos são disponibilizados por 1 ingresso
1/n eventos são apresentados por 1/n  palestrantes

1/n palestrantes apresentam 1/n eventos

1/n apps disponibilizam 1/n e-books
1/n apps disponibilizam 1/n audiobooks

1/n e-books são disponibilizados por 1/n apps

1/n audiobooks são disponibilizados por 1/n apps




