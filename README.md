# Caesar Challenge
Um de nossos desenvolvedores estava estudando sobre Cifra de César e resolveu aplicá-la no nosso algoritmo de gerar chaves de APIs, mas no meio dos seus estudos, acabou não prestando atenção e modificou todas as chaves de API do nosso banco de dados!

Infelizmente ele não lembra o algoritmo que usou, mas sabemos que toda chave de API, depois de descriptografada, contém um texto legível; por exemplo: `TresPratosDeTrigoParaTresTigresTristes`.

Para gerar uma API_KEY nova, basta fazer um GET na rota [https://challenge.pagar.me/key](https://challenge.pagar.me/key) enviando algum e-mail:
```
  GET /key?email=teste@teste.com HTTP/1.1
  Host: challenge.pagar.me
```
Lembnrando que a API_KEY que você receberá desse request está criptografada!

Como uma pessoa que desenvolve, a sua missão é descriptografá-la para conseguir fazer login em nossos sistemas, de maneira **automatizada**, para que qualquer pessoa consiga reverter a própria chave de API utilizando a sua ferramenta.

Para fazer login no nosso sistema desse teste, basta fazer um POST na rota [https://challenge.pagar.me/login](https://challenge.pagar.me/login) usando o seu e-mail e a chave de API (descriptografada) como parâmetros:
```
POST /login HTTP/1.1
Host: challenge.pagar.me
Content-Type: application/json
{ 
    "email": "teste@teste.com", 
    "api_key": "API_KEY_TresPratosDeTrigoParaTresTigresTristes"
}
```

*Sinta-se livre para usar a linguagem que quiser!*
