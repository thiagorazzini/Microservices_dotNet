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

![[Pasted image 20231105162852.png]]

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
