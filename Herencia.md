Herencia
La herencia en CSS es el mecanismo mediante el cual determinadas propiedades de un elemento padre se transmiten a sus hijos
No todas las propiedades CSS son heredadas, porque algunas de ellas no tendría sentido que lo fueran.
Por ejemplo, los relacionados al tamaño de los elementos.
​
​
Lista completa de las propiedades de CSS, sí se heredan o no.
https://www.w3.org/TR/css-2010/#properties
​
​
​
​
​
Herencia
Todos los elementos de un documento HTML heredan todas las propiedades heredables de su padre excepto el elemento raíz (html), que no tiene padre.
El valor por defecto para estas propiedades es inherit.
p { color: inherit; } /*valor por defecto, hereda el color del div, que lo hereda del body, que lo hereda del html*/
​
​
​Escribir menos código.
Si ponemos la font-family al elemento HTML, todos los elementos lo heredan, no tengo que reescribirlo para que otros lo tengan.
​
¿Que pasa cuando a un elemento tiene 2 estilos definidos pero diferentes?
​
​
​
​
​
Cascada - Especificidad
Más específico es el selector, entonces ese es el estilo que se aplica.
​

Especificidad en selectores anidados
Lo que tiene clases es más específico que lo que no.
Si tienen la misma cantidad de clases, gana el que tiene más elementos para cumplir.
Especificidad en selectores anidados

Cascada - Orden
Si dos declaraciones afectan al mismo elemento, tienen la misma importancia y la misma especificidad, la selección final es el orden en las fuentes.
La declaración que se ve después en las hojas de estilo "ganará" a las anteriores.
​
​
​
No hay colisiones, porque no coinciden las propiedades en CSS. Hay herencia de estilo.
Ejemplo 2
Ahora hay colisiones,
¿Qué sucede?
Como ver las colisiones en Chrome
Se indican tachadas, las propiedades que colisionaron y “perdieron”.
Buena Práctica
D.R.Y. – Don’t Repeat Yourself
One principle of development is D.R.Y., also known as don’t repeat yourself. Within CSS this principle can speak volumes as it is easy to continually write the same styles over and over again. Don’t. CSS was designed in a way to allow you to cascade styles and use classes so that you easily apply and inherent styles. The end goal is to write clean and light code, of which is semantic and easily managed.
​
​
Ejercicio
Realicen una página:
Elementos anidados.
Utilizar selectores anidados para dar estilos.
Probar colisiones y ver qué estilo se impone.
​
​
​
​
​
​
Cross Browser
Consejos para desarrollar páginas X-browser
Cada navegador soporta diferentes cosas
Usar propiedades específicas y debajo las estándar
-webkit-border-radius: 5px; //Chrome
border-radius: 5px; //estándar
Así el estándar reemplaza al específico una vez que tiene soporte
Probar cada versión en todos los navegadores objetivo, no desarrollar en uno y arreglar al final en los demás (es más difícil y costoso)
¿Qué soporta cada navegador?
La practica hace al maestro (y el maestro se tiene que actualizar diariamente).
