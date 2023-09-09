
## [React](https://es.react.dev/)

Es una biblioteca de javascript de código abierto para contruir interfaces de usuario. 
Esta basado en componentes. La interfaz se divide en componentes independientes, que continen su propio estado, cuando el estado de un componente cambia, React vuelve a renderizar la interfaz.

Esto hace que React sea una herramienta muy útil para construir interfaces complejas, ya que permite dividir la interfaz en piezas más pequeñas y reutilizables.

Es una biblioteca muy popular y es usada por muchas empresas como Facebook, Netflix, Airbnb, Twitter, Instagram, etc.

### Características

- **Componentes**: React está basado en componentes, que son unidades de código reutilizables que se pueden combinar para crear interfaces de usuario complejas.

- **DOM virtual**: React utiliza un DOM virtual para renderizar los componentes. El DOM virtual es una representación en memoria del DOM real, lo que permite a React actualizar la interfaz de usuario de forma eficiente.

- **Declarativo**: React es declarativo, lo que significa que se centra en lo que debe hacerse, en lugar de cómo hacerlo. Esto hace que el código sea más fácil de entender y mantener.

- **Unidireccional**: React utiliza un flujo de datos unidireccional, lo que significa que los datos fluyen de los componentes padres a los componentes hijos. Esto ayuda a evitar errores y a mantener el código ordenado.

- **Universal**: React se puede ejecutar tanto en el cliente como en el servidor. Esto permite crear aplicaciones web que se cargan rápidamente y funcionan bien en todos los dispositivos.


## ¿Qué es un componente?

Un componente es una pieza de código que renderiza una parte de la interfaz. Los componentes pueden ser parametrizados, reutilizados y pueden contener su propio estado. Un componente puede ser tan pequeño como un botón o tan grande como toda una página web.

En React los componentes se crean usando funciones o clases que retornan elementos que están escritos en la sintaxis de JSX, estos elementos cuando react los renderice se convertirán en elementos HTML.

### ¿Qué es JSX?

JSX es una sintaxis de JavaScript que combina HTML y JavaScript para simplificar la creación de interfaces de usuario en aplicaciones web, especialmente en el contexto de React. Facilita la legibilidad del código y la construcción de componentes reutilizables. 

### ¿Qué son los props?

Los props (propiedades) en React son un mecanismo esencial para pasar datos de un componente padre a un componente hijo, lo que permite la construcción de aplicaciones modulares y reutilizables. Facilitan la configuración y personalización de componentes y promueven la comunicación eficiente entre diferentes partes de una aplicación React.

## Eventos en React

los eventos son acciones que ocurren en la interfaz de usuario, como hacer clic en un botón, mover el mouse sobre un elemento o presionar una tecla en el teclado. Puedes gestionar estos eventos en tus componentes React para controlar el comportamiento de tu aplicación. Algunos de ellos son:

- onClick: Click
- onMouseOver: Pasar el mouse por encima
- onMouseOut: Sacar el mouse de encima
- onChange: Cambio de valor en un input
- onSubmit: Envio de formulario
- onKeyDown: Tecla presionada
- onFocus y onBlur: Enfocar y quitar foco del elemento

### ¿Qué es el estado?

El estado (state) en React es un concepto fundamental que se utiliza para almacenar y gestionar datos que pueden cambiar a lo largo del ciclo de vida de un componente. El estado permite a los componentes React mantener y reflejar información dinámica, lo que los hace interactivos y capaces de responder a eventos y cambios en los datos.

``` javascript
import React, { useState } from 'react';

function Contador() {
  const [contador, setContador] = useState(0);

  const aumentarContador = () => {
    setContador(contador + 1);
  };

  return (
    <div>
      <p>Contador: {contador}</p>
      <button onClick={aumentarContador}>Aumentar</button>
    </div>
  );
}

```

