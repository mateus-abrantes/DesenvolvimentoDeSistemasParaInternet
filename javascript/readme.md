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
recuperando valores dos 2 inputs e enviando para a função soma e exibindo o resultado na div resultado.
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
      function sub(x, y)
       { 
         var resultado = x-y;
         return resultado;
       }
      function mult(x, y)
       { 
         var resultado = x*y;
         return resultado;
       }
      function div(x, y)
       { 
         var resultado = x/y;
         return resultado;
       }
       function pegarValores(operacao) {
         var a = parseInt(document.getElementById("a").value);
         var b = parseInt(document.getElementById("a").value);
         if(operacao==1) 
           var result_soma = soma(a,b);
         if(operacao==2) 
           var result_soma = sub(a,b);
         if(operacao==3) 
           var result_soma = mult(a,b);
         if(operacao==4) 
           var result_soma = div(a,b);
           
         document.getElementById("resultado").innerHTML=result_soma;
       }
       
    </script>
    <script src="myscript.js"></script>
  </head>
  <body>
      <div id="resultado"></div>  
      A:<input id="a" type="text"></br>
  B:<input id="b" type="text"></html></br></br>
      <button onclick="pegarValores(1)">
        +
      </button>
      <button onclick="pegarValores(2)">
        -
      </button>
      <button onclick="pegarValores(3)">
        *
      </button>
      <button onclick="pegarValores(4)">
        /
      </button>
  
  </body>
</html>
```

## Calculadora em Jquery
```javascript
<!DOCTYPE html>
<html>
  <head>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script> 
    <script>
       function soma(x, y)
       { 
         var resultado = x+y;
         return resultado;
       }
      function sub(x, y)
       { 
         var resultado = x-y;
         return resultado;
       }
      function mult(x, y)
       { 
         var resultado = x*y;
         return resultado;
       }
      function div(x, y)
       { 
         var resultado = x/y;
         return resultado;
       }
      
      $(document).ready(function(){
        $("#btsoma").click(function(){
          var a = parseInt($("#a").val());
          var b = parseInt($("#b").val());
          $("#resultado").html(soma(a,b));
        });
        $("#btsub").click(function(){
          var a = parseInt($("#a").val());
          var b = parseInt($("#b").val());
          $("#resultado").html(sub(a,b));
        });
        $("#btmult").click(function(){
          var a = parseInt($("#a").val());
          var b = parseInt($("#b").val());
          $("#resultado").html(mult(a,b));
        });
        $("#btdiv").click(function(){
          var a = parseInt($("#a").val());
          var b = parseInt($("#b").val());
          $("#resultado").html(div(a,b));
        });
      });
    </script>
  </head>
  <body>
      <div id="resultado"></div>  
      A:<input id="a" type="text"></br>
      B:<input id="b" type="text"></br></br>
      <button id="btsoma">+</button>
      <button id="btsub">-</button>
      <button id="btmult">*</button>
      <button id="btdiv">/</button>
  </body>
</html>
```

## HTML consumindo json via ajax
```javascript
<!DOCTYPE html>
<html>
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
<script>
$(document).ready(function(){
  $.ajax({
    url: 'https://randomuser.me/api/',
    dataType: 'json',
    success: function(data) {
      console.log(data);
      $("#resultado").html("nome:"+data.results[0].name.first);
      $("#resultado").append("<br>username:"+data.results[0].login.username);
      $("#resultado").append("<br>celular:"+data.results[0].cell);
      $("#resultado").append("<br><img src='"+data.results[0].picture.large+"'/>");
    }
  });
});
</script>
</head>
<body>
<div id="resultado"></div>
</body>
</html>
```

## APIs publicas

https://randomuser.me

https://any-api.com

