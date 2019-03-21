# Javascript

## Introduçao ao Javascript

utilizar o w3schools para criar uma página com validação de formulario
https://www.w3schools.com/js/default.asp
## Criar uma calculadora em javascript

Função SOMA e formulário
```javascript
<!DOCTYPE html>
<html>
  <head>
    <script>
       function soma(x, y)
       { 
         var resultado = x+y;
         return resultado;
       }      
       var x = soma(10,20);
       console.log(x);
    </script>
  </head>
  <body>
      <div id="resultado"></div>  
      A:<input id="a" type="text"></br>
      B:<input id="b" type="text">
      <button>
        SOMA
      </button>
  </body>
</html>
```
recuperando dados do formulario
```javascript
<!DOCTYPE html>
<html>
  <head>
    <script>
       function soma(x, y)
       { 
         var resultado = x+y;
         return resultado;
       }
       function pegarValores() {
         alert(document.getElementById("a").value);
       }
       
    </script>
    <script src="myscript.js"></script>
  </head>
  <body>
      <div id="resultado"></div>  
      A:<input id="a" type="text"></br>
      B:<input id="b" type="text">
      <button onclick="pegarValores()">
        SOMA
      </button>
  </body>
</html>
```

```javascript
<!DOCTYPE html>
<html>
  <head>
    <script>
       function soma(x, y)
       { 
         var resultado = x+y;
         return resultado;
       }
       function pegarValores() {
         var a = parseInt(document.getElementById("a").value);
         var b = parseInt(document.getElementById("a").value);
         var result_soma = soma(a,b);
         document.getElementById("resultado").innerHTML=result_soma;
       }
       
    </script>
    <script src="myscript.js"></script>
  </head>
  <body>
      <div id="resultado"></div>  
      A:<input id="a" type="text"></br>
      B:<input id="b" type="text">
      <button onclick="pegarValores()">
        SOMA
      </button>
  </body>
</html>
```

## APIs publicas

https://randomuser.me

https://any-api.com

