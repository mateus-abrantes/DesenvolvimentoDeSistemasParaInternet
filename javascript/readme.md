# Javascript

## Introduçao ao Javascript

utilizar o w3schools para criar uma página com validação de formulario
https://www.w3schools.com/js/default.asp
## Criar uma calculadora em javascript

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
    <script src="myscript.js"></script>
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

## APIs publicas

https://randomuser.me

https://any-api.com

