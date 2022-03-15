# 01-intro-react

# 1 Creamos el `index.hmtl`
~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ReactApp</title>
</head>
<body>
    
</body>
</html>
~~~

Copiamos estas tres librerías en el archivo `index.html`
para cargar las liberías de React
~~~html
 <script crossorigin src="https://unpkg.com/react@16/umd/react.production.min.js"></script>
    <script crossorigin src="https://unpkg.com/react-dom@16/umd/react-dom.production.min.js"></script>
    <script src="https://unpkg.com/babel-standalone@6/babel.min.js"></script>
~~~

# 2 Creamos nuestro primer hola mundo
- Añadimos esto al `index.html`
~~~html
<body>
    <div id="root"></div>
    <script type="text/babel">
        const divRoot = document.querySelector('#root');
        const h1Tag = <h1>Hola Mundo</h1>;

        ReactDOM.render(h1Tag,divRoot);



    </script>
</body>
~~~
- Ponemos una variable `nombre` dentro de un tag de html
~~~html
<body>
    <div id="root"></div>
    <script type="text/babel">
        const divRoot = document.querySelector('#root');

        const nombre = 'Patricia';
        const h1Tag = <h1>Hola, soy {nombre}</h1>;

        ReactDOM.render(h1Tag,divRoot);



    </script>
</body>
~~~

# 3 Babel
Nos ayuda a la compatibilidad del código de react para los navegadores

https://babeljs.io/
~~~js
const resApi = {
  personajes: ['Goku','Vegeta']
}
console.log(resApi.personajes.lenght)
~~~

Probamos este código y nos da error cuando personajes viene vacío, undefined.
Entoces vamos a cambiarlo:
~~~js
const resApi = {
  personajes: ['Goku','Vegeta']
}
console.log(resApi.personajes?.lenght)
~~~
React no depende de Babel, con el jsx elimina esa depencia. Pero si trabajamos en javascript si tenemos que tener en cuenta babel.
