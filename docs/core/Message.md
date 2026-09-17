


## Modelo de Message

Esse documento trata de como deve ser formatada o modelo do message que vem da interface, passa pelo core e então é enviada para o Mia AI.s

#### O que é o message?
É responsável por enviar a mensagem do usuário para o core, onde processamento pode ser feito e então entregue para a AI como prompt.

Por conta disso, esse arquivo pode ser separado em duas etapas. Uma entre a interface e o core e outra do core para o Mia AI.

Esse json deve incluir os seguintes fields:

`String: message` É o conteúdo da mensagem em si. Obrigatório. É o que o usuário digita.

`String: conversation_id` É o id que identifica a conversa com o usuário. Obrigatório.

`String: user_id` É o id que identifica o usuário. Obrigatório.

A interface deve esperar por códigos de HTTP dependendo no resultado da transferência.

`200` Sucesso.

`400` Json inválido.

`500` Erro interno.