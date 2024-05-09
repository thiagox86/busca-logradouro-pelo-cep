Busca Endereço pelo CEP: Encontre informações de endereços a partir do CEP informado. Nosso serviço online permite buscar detalhes como logradouro, bairro e localidade.

E além do nosso serviço de buscar informações de logradouro pelo CEP, você que é desenvolvedor pode estudar o código fonte utilizado para o desenvolvimento desta pequena aplicação web e os conceitos utilizados para tal.

Busca Endereço pelo CEP explicado:
Temos aqui uma aplicação web que permite aos usuários buscar informações de endereços a partir de um CEP informado. Vou explicar o que cada parte faz:

Estilos CSS:
Define estilos para os elementos HTML.
#tr-div-cep e #tr-div-cep input têm largura de 100% e margem inferior de 25px.
A tabela e suas células (table, th, tr, td) têm bordas de 1px, alinhamento central e espaçamento interno de 15px.
HTML:
Cria um campo de entrada para o usuário digitar o CEP (<input>).
Dois botões:
“BUSCA ENDEREÇO”: Quando clicado, aciona a função buscaLogradouro(), que faz a busca das informações do logradouro segundo o CEP informado;
“LIMPAR BUSCA”: Quando clicado, aciona a função limpaBusca(), que apaga da tela todas as tabelas criadas e ainda limpa o campo de entrada do CEP;
JavaScript:
A função apenasNumeros(e) permite apenas a digitação de números no campo de entrada.
A função buscaLogradouro() é acionada quando o usuário clica no botão “BUSCA ENDEREÇO”:
Verifica se o CEP foi informado e tem 8 dígitos.
Se sim, faz uma requisição AJAX para o serviço ViaCEP (URL construída com o CEP informado).
Se o CEP não for encontrado, exibe um alerta.
Caso contrário, cria uma tabela com os dados retornados (CEP, DDD, logradouro, bairro, localidade e UF).
Tabela de Resultados:
A tabela é criada dinamicamente no JavaScript.
O cabeçalho contém as colunas: “CEP”, “DDD”, “Logradouro”, “Bairro”, “Localidade” e “UF”.
Os dados obtidos da requisição são preenchidos nas células correspondentes.
