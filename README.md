# __Sistema para controle de Despesas__ <h1>

## __Introdução__ <h2>

#### No mundo de hoje, onde as finanças pessoais e empresariais desempenham um papel vital na nossa vida quotidiana, a necessidade de um sistema eficiente de gestão de gastos e pagamentos é inegável. Um sistema bem concebido e intuitivo pode ajudar os utilizadores a gerir as suas finanças de forma mais eficaz, organizando e exibindo claramente os seus gastos, acompanhando os pagamentos e ajudando-os a conciliar os seus gastos. Desta forma este documento elaborado tenda explanar sobre a criação de um  projeto visado para controle de despesas, para tal seguiremos nas próximas linhas com as funcionalidades do mesmo. <h4>

## __Descrição das funcionalidades__ <h2>

### __Entrada de despesas__ <h3>
#### Permite que o usuário final otimize os registros de suas despesas podendo estas serrem categorizadas ou não, assim facilitando o acompanhamento de tais atividades forma organizada e eficiente, lembrando que para tal função, serão informados dados simples como descrição, valor, data de vencimento e categoria  <h4>

### __Anotar Pagamento__ <h3>
#### Apos o usuário realizar um pagamento, tal funcionalidade serve para se manter o registro financeiro sobre tal despesa paga, isso serve de forma geral para assegurar que as despesas devidas sejam devidamente pagas, proporcionado ao usuário uma visão clara sobre as finanças, desta foma permitindo um planejamento adequado sobre os pagamentos a serem realizados.   <h4>

### __Listar Despesas__ <h3>
#### Nesta função o usuário tera a opção de visualizar e gerenciar suas contas, de acordo a necessidade. Sendo que as opções. edição, e exclusão e retorno ao menu principal  estarão dispostas para melhor atender o cliente final, permitindo que os registros sempre estejam precisos e atualizados de forma organizada contando com a capacidade de filtrar as contas por critérios.  <h4>

### __Gerenciar Tipos de Despesa__ <h3>
#### Quando o usuário define e personaliza os tipos de contas em categorias conforme relevância, tal função organiza as despesas em camadas que tornam muito mais eficiente quando se deseja filtrar algo ou gerar relatórios de gastos. <h4>

### __Gerenciar Usuários__ <h3>
#### Aqui o usuário tem a garantia que suas informações estarão seguras, visto que a função de gerenciar usuários é fundamental para a garantia e controle de acesso ao software em si, pois é nesta fase que são definidos tipos de usuários e suas senhas que são criptografadas, funcionalidade esta que é fundamental para garantir segurança e acesso de controle ao sistema<h4> 

## __Visão geral__ <h2>
#### Eleita as funcionalidades do software, a próxima etapa para desenvolvimento do mesmo, parte da aplicação dos conceitos de engenharia de software, onde se aplicam modelos de desenvolvimento, mas para tal ainda ficaremos com as definições de metodos utilizados em POO ( Programação Orientada a Objeto). Sendo assim daremos início as classes que serão utilizadas neste software.  <h4>

## __Definição de classes__ <h2>
#### Tendo como base a POO, que tem intuito a abstração de objetos do mundo real para o computacional. Para o desenvolvimento do software em questão utilizaremos classes, com base que estas quando bem definidas, ajudam a organizar e estruturar as  informações e as funcionalidades de um sistema de maneira correta.<h4>

### __1. Classe Despesa__ <h3>
#### tal é responsável por representar a conta de forma individual, sendo que aqui são definidos tributos como descrição, data de vencimento, tipo de despesa, se a mesma encontra-se aberta ou paga e um identificador do tipo ID. Para tal deve se utilizar métodos de getters e setters para os atributos, além disto a mesma deve contar com encapsulamento pois toda a regra de negócio deve estar protegida, para que não se possa alterar dados de forma indiscreta. <h4>

### __2. Classe Controle__ <h3>
#### esta deve atuar de maneira principal pelo sistema, pois contem funções e métodos específicos, como adicionar despesa, gerenciar tipos de despesas, gerenciar usuários, registrar pagamentos. Para tal vai contar com métodos como, listar despesas em geral, listar despesas pagas, listar despesas em aberto, gerenciar usuários, gerenciar despesas. Assim como tera os seguintes atributos, lista de pagamentos, lista de tipos de despesas, lista de usuários, lista geral de despesas.<h4>

### __3. Classe Usuário__ <h3>
#### como o próprio nome já diz, é responsável por representar o usuário final do sistema, sendo responsável por gerir informações pertinentes do usuário como nome, nome de usuário, informações de contato, cadastro de local para envio de senha, cadastro para reenvio de redefinição de senha, e, por fim, um identificador único (ID), além disso fara utilização  getters e setters para os atributos.<h4>

### __4. Classe Pagamento__ <h3>
#### esta representa o pagamento de uma conta, no caso da despesa em si, permitindo ao usuário que verifique através de relatório se esta foi paga ou não de forma integral ou parcial, para tal conta com atributos como valor da despesa, tipo de pagamento ( a vista, parcelado) valor pago, data do pagamento e por fim o identificador ID, além disso os métodos serão composto por getters e setters.<h4>

### __5. Classe Tipo de Despesa__ <h3>
#### tal classe serra responsável, por categorizar a despesa em tipos ou subtipos a fim de se ter um melhor controle, sendo que tal funcionalidade e essencial  para uma melhor otimização do sistema garantindo um relatório mais especifico de acordo com a categoria desejada, para tal se deve utilizar os métodos  getters e setters para os atributos de nome, descrição<h4>.

### __Herança__ <h3>
#### Tendo as classes já definidas, podemos então pensar no quesito de herança que é utilizado na POO, para tal após análise das classes já escolhidas, podemos elencar a seguinte classe para ser aplicada técnica de herança. Classe Tipo de Despesa: utilizando os conceitos de POO podemos verificar que esta classe se encaixaria perfeitamente para utilização de herança visto que tipo de despesa é algo bem genérico, e pode se categorizado em subcategorias mais concretas. Para tal se deve criar uma classe abstrata chamada tipo de despesa, que engloba vários aspectos comuns que podem ser encapsulados, a todas subcategorias, desta forma podem ser definidas subcategorias que iram herdar da classe mãe. <h4>

### __Interfaces e Polimorfismo__ <h3>
####  Seguindo os conceitos de POO, podemos dizer que o polimorfismo está relacionado a questão de que quando temos muitas subcategorias que vem da classe pai, vão se portar como  mesma, e para tal a implementação neste software a princípio ficaria através da implementação das interfaces, pois assim poderemos fazer com que vários objetos se comportem como um só. Quando aplicamos a interface e polimorfismo crimos uma estrutura que permite tratar objetos diferentes como se fossem do mesmo tipo, para tal implementaremos a interface na classe tipo de despesa, pois as classes herdeiras que serão concretas como transporte, diversão, mercado entre outras, implementaria uma interface chamada de Despesa por categoria, onde um método responsável por calcular o limite de gasto possa ser implementado pela classe pai. <h4>

### __Sobrecarga e Sobrescrita de Método Construtor__ <h3>
#### Quando falamos de método construtor devemos pensar diretamente em sobrescrita de método, pois com essa prática podemos fazer algumas implementações visando este software em específico, como aplicar o método nas subclasses para de forma direta personalizar o comportamento das mesmas em relação as despesas com vários detalhes, para tal devemos crias um método que permita criar as instâncias da classe despesa, sendo que tal deve ter diferentes detalhes, mesmo que não sejam definidos seus atributos por completo, quando esta for diretamente criada, para tal a sobrescrita do método nas subclasses permite de forma direta personalizar a  criação do objeto, tendo como norte a base da categoria despesas. <h4> 

### __Métodos e Atributos Estáticos__ <h3>
#### Para tal será utilizado um atributo estático chamado despesas_cont, do qual ira facilitar rastreamento das instancias das despesas que forem criadas durante o uso do programa, desta forma podemos dizer que a implementação desta ferramenta é utel para ajudar a manter informações que se aplicam a classe toda vez que esta é instanciada. <h4>

### __Criptografia de Senhas__ <h3>
#### Quando falamos de criptografia de senhas devemos ter em mente que tal técnica esta relacionada diretamente a questões como vazamento de senhas, mitigação de risco portanto tal método desenvolvido deve ser muito crucial pois ira proteger a segurança referente as informações do usuário final, para tal o programa em si contara com um método responsável por verificar as senhas, do qual se chamara senhas_verificadas, do consiste basicamente em comparar a senha digitada pelo usuário com a senha já cadastrada por este e criptografada pelo sistema.  <h4> 
