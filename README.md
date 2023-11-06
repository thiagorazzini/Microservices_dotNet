<h3>O que são werbservices ?</h3>


Webservices são aplicações que compartilham informações entre outas e é hospedada em um servidor onde ela pode ser acessada através do protocolo HTTP. Os clientes que são mais comummente usados como meio de acesso com o protocolo HTTP são os browsers, mas também pode ser feita requisições através de um browser, de um client e até mesmo por linha de comando (powershell ou linux). 

<h4>Simplificando a explicação</h4>

Webservices são somente legíveis por maquinas ou por outros sistemas, usando um exemplo do dia a dia:

Um carro corsa utiliza o filtro de ar do modelo A47b, então esse mesmo filtro pode ser reaproveitado para outo modelo de carro como por exemplo o Cruze. É a ideia de reutilização do services  e usando essa ideia em desenvolvimento de software, teremos a seguinte ideia:
Imagine o desenvolvimento de uma aplicação webservice que faça a busca e validação do CPF, uma aplicação desktop pode usar essa aplicação para esse tipo de ação, da mesma forma que uma aplicação mobile pode fazer o mesmo. Tudo isso acontece utilizando o HTTP!


<h4>SOAP x REST</h4>
Diferenças de protocolo entre elas:
 - SOAP utiliza o HTTP para fazer chamadas RPC trafegando XML
 - REST utiliza o HTTP para fazer as chamadas e suporta diferentes formatos de arquivo

![image](https://github.com/thiagorazzini/Microservices_dotNet/assets/30513646/9233702d-50a6-4140-ad47-545dcb765e2a)

<h4>O que é REST ?</h4>
Estado representacional de transferência

REST tem suas restrições, são elas:

![[Pasted image 20231105170601.png]]

Vantagens de utilizar o REST
![[Pasted image 20231105170830.png]]


<h4>Entendendo  Request e Response</h4>
Para entender o request, vamos pegar o exemplo de um uso diário que é a utilização do Chrome, quando  executamos o uso para acessar um site, realizamos  o HTTP request  e o servidor vai até a base de dados, faz a ação de acordo com o verbo http que foi realizado o request e devolve utilizando utilizando o HTTP response.
![[Pasted image 20231105171656.png]]


Represetando uma request:
![[Pasted image 20231105171823.png]]

Representando o response:
![[Pasted image 20231105171900.png]]

<h4>Os tipos de parâmetros usados no REST</h4>

<strong>Paths params:</strong>
Parâmetros que são passados pela URL e que são obrigatórios, caso não exista esses parâmetros será lançado uma exceção ou fará um operação similar mas que utiliza o mesmo verbo.

Exemplo

![[Pasted image 20231106075939.png]]

podemos entender nessa URL a existência de 3 parâmetros na busca de livros:
1 - asc: Ordenação crescente do nome dos livros;
2 - 10: 10 itens por página;
3 - 1: Index da página acessada

<strong>Query params:</strong>

Parâmetros passados por URL  mas não obrigatórios, então iniciamos a URL como já conhecido e colocamos um ponto de interrogação,  após a interrogação inserimos os parâmetros desejado

![[Pasted image 20231106080349.png]]

Entendendo os parâmetros, ficaria assim:
- firstName=Clean: primeiro colocamos o nome do parâmetros, depois o sinal de atribuição e em seguida o valor.
- Para colocar mais parâmetros, devemos inserir o & e repetir nome do parâmetro, sinal de atribuição "=" e o valor do parâmetro

<h4>Header Params</h4>
São enviados no cabeçalho da requisição, eles não podem ser enviados via browser, devemos utilizar um client(postman), nele podemos colocar algumas keys como tipo de arquivo(Accept), Content-Type, Authorizathion.


![[Pasted image 20231106081056.png]]

<h4>Parâmetros do body</h4>
São usados para envio de informações completas, podendo ser enviado via JSON e entre vários outros formatos aceito pela API REST  .

Exemplo utilizando JSON:
![[Pasted image 20231106081226.png]]

<h4>HTTP Status Code</h4>
Aqui podemos encontrar o retorno da ação realizada, para verificar o que aconteceu depois da demanda ser executada:

São 5 tipos de status code:
![[Pasted image 20231106082038.png]]


Status code 2xx Sucesso muito utilizados:
![[Pasted image 20231106082147.png]]

Status code 4xx Erro do client:
![[Pasted image 20231106082403.png]]

400: Retornado quando o client envia um request que não existe
401: sem autorização
403: Client não tem autorização para aquele endpoint 
404: Retornado quando o endpoint não é encontado

<strong>HTTP Status Codes em Serviços REST</strong>


Destacando os mais vistos no dia a dia

200 OK - Criação ou deleção executada com sucesso
201 Created: Criação de uma fila, tópico ou qualquer coisa que será executada posteriormente para ser executada/consumida
204 No content: Deleção de uma fila, tópico, sessão bem sucedida mas sem retorno de conteúdo

400 Bad Reques: Client faz endereço errado, ou uma busca de Id que não existe mais ai retorna um bad request.
401 Unauthorized: Cliente sem autorização para executar a requisição na operação em questão.
403 Forbiden: Não tem permissão para executar a requisição em questão.
404 Not Found: Não encontrado o item que foi buscado pois o objeto não existe
405 Mathod Not Allowed - O usuário não tem permissão de acesso que foi submetido
409 Conflict: Ja existe o objeto criado e voce esta tendando criar o mesmo objeto


500 Internal Erro de Server: Ocorreu um erro de execução no servidor
