## Broken Access Control 

Broken Access Control refere-se à possibilidade de um usuário, seja por meio da modificação de uma URL, cookie, token ou pelo conteúdo de uma página, acessar dados aos quais não deveria ter acesso. 

O usuário pode acessar os dados referentes a outra pessoa e/ou elevar suas permissões de um usuário comum para um administrador ou superusuário.

#### Exemplos: 

1- Dado uma URL como <code>www.example.com/orders/orderid=900</code>, o que aconteceria se alterássemos esse orderid por **1**? 
E se um usuário tentasse acessar <code>www.mysite.com/orders/orderid=901</code>.

Provavelmente haverá um código para verificar se um usuário está conectado (provavelmente um atributo Authorize simples no .NET Core).


2 - Um atacante pode alterar uma URL para forçar algum acesso. Admin rights are required for access to the admin page.
<code>http://example.com/app/getappInfo</code>

<code>http://example.com/app/admin_getappInfo</code>


#### Vulnerabilidades Broken Access Control podem ser:

- Bypass no controle de acesso modificando a URL, alterando a aplicação, alterando a página HTML e/ou usando uma ferramenta de ataque. 
- Escalação de Privilégio, seja tendo permissões de usuário sem estar conectado, seja como ter permissões de administrador em um usuário comum. 
- Manipulação de Metadados, criar ou alterar tokens como JSON Token Web (JWT), alterar cookies ou campos ocultos afim de elevar privilégios. 
- Configuração incorreta do CORS que permite que pessoas não autorizadas tenham acesso a API. 
- Acesso a APIs com controle de acesso ausentes para POST, PUT e DELETE. 

#### Formas de prevenir:




#### Referências:
* OWASP Application Security Verification Standard: V4 Access Control
* OWASP Testing Guide: Authorization Testing
* OWASP Cheat Sheet: Access Control
* CWE-284: Improper Access Control (Authorization)
* CWE-285: Improper Authorization
* CWE-639: Authorization Bypass Through User-Controlled Key
* PortSwigger: Exploiting CORS misconfiguration
