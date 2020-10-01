[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

![logo](https://github.com/falso-de-verdade/requisitos/raw/master/logo.jpg)

# Introdução

No projeto será abordado uma solução para o controle de moradores em determinadas dependências de um condomínio, prevenindo assim a aglomeração de pessoas em locais onde o limite de indivíduos deve ser respeitado no momento que estamos vivenciando. Seguindo também as normas do condomínio para que todos os moradores possam usufruir de locais compartilhados.

O sistema contará com uma interface amigável e de fácil utilização, onde qualquer morador pode realizar um agendamento de alguma dependência do condomínio além de estar ciente das normativas e reuniões do condomínio.

### Requisitos funcionais
#### Essenciais
Serão apresentados os requisitos pelos quais o programa exige para o funcionamento completo.

1. Cadastro de usuário

O sistema deve permitir o cadastro de dois tipos de usuário: um síndico, responsável por administrar um condomínio, ou um morador, que pode solicitar o uso de benfeitorias de um condomínio.

2. Cadastro de síndico

Ao selecionar a opção de cadastrar-se como síndico, este deve preencher suas informações de:

- Nome
- Endereço de email
- Senha usada para acesso ao sistema

3. Cadastro de morador

O morador deve buscar por um convite do usuário síndico, para assim registrar-se no condomínio. Este convite deve ser compartilhado com o morador previamente, sendo composto por um endereço web. No cadastro posterior ao recebimento do convite, devem ser informados:

- Nome do responsável
- Endereço de email
- Senha usada para acesso ao sistema

4. Cadastro de condomínio

Um usuário do tipo síndico pode cadastrar um ou mais condomínios, informando dados suficientes para que um morador tenha confiança de que está sendo adicionado ao condomínio correto. São informados:

- Nome do condomínio
- Endereço do condomínio - opcional
- Imagens do condomínio - opcional
- Comentário sobre regras do condomínio, horário de silencio, etc - opcional

5. Cadastro de dependência

Um usuário do tipo síndico pode cadastrar objetos que terão a funcionalidade de representar uma dependência física no condomínio especificado. Tais objetos, também chamados de dependências, devem satisfazer as necessidades e normas impostas pelo condomínio, sendo de responsabilidade dos mesmos pela sua fidelidade. Especificamente, devem ser informados:

- Condomínio em questão
- Nome da dependência
- Local da dependência - opcional
- Disponibilidade de horários
- Limite de pessoas
- Mídia (ex.: fotos, vídeos, documentos) - opcional

6. Cadastro do ticket para troca de agendamento

Ao tentar agendar uma dependência já alocada naquela data, o morador tem a opção de abrir um ticket para ganhar a vez no agendamento.

7. Acesso ao sistema

O usuário que possui suas credenciais de acesso, pode fazer o login no sistema, dando acesso a área interna dos moradores ou do síndico, dependendo das credenciais fornecidas. Os dados de acesso são:

- Endereço de e-mail
- Senha

8. Visualização de dependências

Tanto moradores quanto o síndico poderão visualizar uma listagem das dependências cadastradas no condomínio, tendo cada item as seguintes informações:

- Condomínio em questão

- Nome da dependência
- Local da dependência - opcional
- Disponibilidade geral de horários (sem considerar reservas)
- Limite de pessoas
- Listagem de todas as reservas futuras cadastradas

9. Visualização dos agendamentos

Tanto o morador quanto o síndico poderão ter acesso aos agendamentos marcados, com a diferença de que o morador visualiza apenas os agendamentos marcados por ele, e o síndico, os do condomínio por completo. Especificamente, as informações apresentadas são:

- Dia de ocupação
- Nome da dependência
- Hora inicial e final de ocupação
- Marcador que identifica se o agendamento está por acontecer

10. Visualização de agendamentos das dependências

Tanto morador como o síndico pode visualizar qualquer agendamento feito por qualquer dependência do condomínio em qualquer dia da semana e horário, trazendo uma listagem do agendamento com informações de quem agendou, qual dependência foi alocada, um breve resumo do local agendado, como por exemplo informações do que pode fazer no local e o que é proibido segundo as normas do condomínio e o limite de pessoas. A busca do agendamento deve ser feita pelo dia da semana, dependência do condomínio e horário inicial até hora final do agendamento.

11. Visualização dos moradores pelo síndico

Um usuário síndico visualizará todos os moradores de um determinado condomínio. Especificamente, as informações apresentadas são:
 - Nome do morador
 - Data de entrada
 - Localização do morador
 - Endereço de e-mail do morador

12. Visualização dos conflitos de novos agendamentos pelo sindico

O síndico visualizará todos os conflitos gerados pela desistência de um agendamento. Este tomará uma ação no sentido de definir quem será o morador a ganhar o agendamento. Os dados apresentados serão os seguintes:
 - Nomes dos moradores envolvidos
 - Nome da dependência
 - Data e hora do agendamento

13. Solicitação de ocupação de dependência

Um morador, ao visualizar uma dependência, pode solicitar a reserva para sua ocupação.

Deve informar:

- Dia de ocupação
- Hora inicial e final de ocupação
- Quantidade de ocupantes - sendo possível informar uma quantidade de 1 ou mais, ou selecionar uma opção &quot;Ocupação total&quot;
- Observações - o morador pode cadastrar uma mensagem para explicar algum uso diferente de uma dependência; por exemplo, o uso normal de um campo de futebol seria o de &quot;ocupação total&quot; - porém, é possível que alguém solicite apenas metade do campo para treinamentos, e, com essa informação, outro morador pode solicitar outra ocupação parcial.

14. Agendamentos não confirmados são cancelados

Um morador que não confirmou o agendamento até o último dia do agendamento, terá seu agendamento cancelado por falta de confirmação antecipada. Com isso o local agendado volta automaticamente a ficar disponível para outros moradores.

15. Mensagem de confirmação do agendamento

Após o morador ter agendado uma dependência disponível no sistema, esse envia para o e-mail do morador uma mensagem informando o sucesso no agendamento. Esta mensagem contém também um endereço web com destino ao sistema, mais especificamente na visualização do agendamento, para que, caso o morador não tenha realizado tal agendamento, possa tomar as medidas cabíveis, como desmarcar o agendamento por exemplo.

16. Morador desiste de um agendamento

O morador  poderá desistir de agendamento já realizado. Fazer isso porém implica que outros moradores estarão aptos a agendá-lo, sendo que aqueles que possuirem um ticket para este agendamento, serão informados ao síndico para resolver este conflito. A única exceção é caso apenas um morador tenha o ticket para o agendamento em questão, sendo que assim o morador é alocado automaticamente.

17. Edição de moradores pelo síndico

O usuário síndico poderá atualizar os dados de um morador pela visualização de moradores. Especificamente, os seguintes dados estarão disponíveis:
 - Nome do morador
 - Endereço de e-mail do morador
 - Localização do morador (ex.: Bloco A Nº 505) - opcional

18. Remover morador do condomínio

Um usuário síndico poderá remover um morador de um determinado condomínio, pela visualização de moradores.

19. Tela de escolha de papel

Quando uma pessoa (um endereço de email) tem conta com os dois papéis, de síndico e morador, ele deve escolher qual papel assumir, após a tela de entrada de email e senha.

20. Tela de escolha de condomínio

Quando uma pessoa (um endereço de email) assume o mesmo papel em vários condomínios, ele deve escolher qual condomínio acessar, após a tela anterior (que pode ser a tela da senha, ou a tela de escolha do papel).

#### Desejáveis
Agora serão apresentados aqueles requisitos que melhoram a interaçao com usuário, mas não impactam diretamente nas funcionaliodades em si.

1. Confirmação de uso de uma dependência

O morador deve receber uma mensagem de e-mail pelo sistema, solicitando que o mesmo confirme a presença na dependência agendada. Tal confirmação é enviada com uma antecipação pré definida de 5 dias. A mensagem de e-mail conterá um endereço web, que após acessado informará ao usuário para clicar em um botão que finalmente realiza a confirmação.
**Observação** : o morador não precisa necessariamente estar com a conta logada no sistema.


2. Criar reuniões de condomínio

O usuário síndico cria reuniões do condomínio, e por ser de interesse dos moradores, esses recebem uma notificação no sistema apresentando as informações da reunião agendada. Especificamente, os dados da reunião são:

- Data e hora
- Duração prevista - opcional
- Descrição da reunião (ex.: assuntos abordados)

3. Abrir solicitação para troca de senha do usuário

Caso algum morador já tenha feito o seu cadastro no sistema, porém esqueceu sua senha de acesso, ele pode solicitar uma troca de senha, onde será encaminhado por e-mail um link onde ele irá redefinir uma nova senha.

4. Atualizar a senha de um usuário, dada uma solicitação

O usuário terá acesso a uma página para efetuar a troca da senha, sendo que esta nova senha não poderá ser igual a senha anterior. Especificamente, as informações requeridas são:

- Nova senha
- Confirmação da senha

5. Lembrar a sessão do usuário com acesso ao sistema pelo navegador

Tanto morador como síndico após terem seu acesso definido, podem optar por deixar suas credenciais salvas e não precisarem mais digitar seu login e senha para acessar o sistema.

6. Lembrar seleção de condomínio

Em relação ao requisito funcional 20, ("Tela de escolha de condomínio"), o usuário pode marcar uma seleção dizendo "não perguntar novamente", para que o sistema presuma que o usuário queira que o sistema sempre acesse o mesmo condomínio ao fazer login.

### Requisitos não-funcionais

1. Consentimento mútuo - Essencial

O sistema não tem, sob sua alçada, determinar quem é de fato o síndico responsável por um condomínio; o uso do sistema presume que, se uma pessoa que cadastrou-se como síndico pode enviar convites para que moradores sejam cadastrados, e estes usem das funcionalidades do sistema como subsídio para suas solicitações, então o sistema está sendo usado corretamente.

2. Múltiplas associações - Essencial

O sistema não presume que um usuário é apenas síndico, ou apenas morador; a seleção, no momento do cadastro, de que um usuário é síndico apenas resulta em oferecer permissão inicial para que o usuário cadastre um condomínio.

Com essa filosofia, um usuário pode ser:

- Morador de um ou mais condomínios (moradia e casa de praia, por exemplo)
- Administrador de um ou mais condomínios
- Administrador de um condomínio, e morador de um condomínio diferente.

3. Filosofia de conflitos - Importante

O sistema não presume que a primeira pessoa a solicitar a ocupação será necessariamente aquela que será atendida; outros moradores poderão solicitar dependências que já tiveram a ocupação solicitada, e o síndico terá a capacidade de tratar esse conflito, seja aceitando qualquer uma das solicitações, seja alterando uma ou mais solicitações para compatibilizá-las.

4. Acessível por um navegador - Essencial

O sistema deve ser acessível por qualquer pessoa por meio da world wide web.

5. Desenvolvido usando a linguagem Javascript - Importante

Para uma melhor interação e fluidez para o usuário, deve-se usar uma linguagem dinâmica no navegador. Dessa forma faz-se obrigatório o uso da linguagem.

6. Confidencialidade dos dados do usuário no acesso ao sistema - Importante

Para garantir a confidencialidade das informações trocadas entre cliente e servidor, faz-se obrigatório que o sistema use um protocolo de comunicação que não exponha os dados do usuário.

7. Confidencialidade da senha do usuário - Importante

O sistema deve garantir que a senha criada pelo usuário não seja exposta, em nenhuma situação.

8. Privacidade do usuário - Importante

Os dados do usuário, contidos no sistema, devem estar disponíveis ao mesmo, sendo possível assim a exclusão imediata da conta junto com os dados do mesmo. 

9. Exigências do login - Essencial

Para um usuário poder utilizar o sistema, deve atender às situações:
- ter inserido email e senha corretos
- possuir um papel válido (seja por ter escolhido um, seja por ser apenas morador/apenas síndico)
- possuir um condomínio escolhido (seja por ter escolhido um, seja por estar associado a apenas um condomínio)
