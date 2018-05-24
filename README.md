# Caesar Challenge
Um de nossos desenvolvedores estava estudando sobre Cifra de César e resolveu aplicá-la no nosso algoritmo para gerar chaves de APIs.
Mas, no meio dos seus estudos, acabou não prestando atenção e modificou todas as chaves de API do nosso banco de dados!<br/>
Infelizmente, ele não lembra o algoritmo que usou, mas sabemos que toda chave de API depois de descriptografada contém um texto legível como por exemplo `TresPratosDeTrigoParaTresTigresTristes`<br/>
Para gerar sua API_KEY, basta fazer um GET na rota [challenge.pagar.me/register](http://challenge.pagar.me/register) usando seu e-mail como parâmetro:
```
  GET /register?email=teste@teste.com HTTP/1.1
  Host: challange.pagar.me
```
Que você receberá sua chave de API criptografada

Como uma pessoa que desenvolve, sua missão é descriptografá-la para conseguir fazer login em nossos sistemas, de maneira **automatizada** para que qualquer pessoa consiga reverter a própria chave de API utilizando sua ferramenta.<br/>

*Sinta-se livre para usar a linguagem que quiser.*

Para fazer login no sistema, basta fazer um POST na rota [challenge.pagar.me/login](http://challenge.pagar.me/register) usando seu email e chave de API como parâmetros:
```
POST /login HTTP/1.1
Host: challenge.pagar.me
Content-Type: application/json
{ 
    "email": "teste@teste.com", 
    "api_key": "API_KEY_TresPratosDeTrigoParaTresTigresTristes"
}
```
