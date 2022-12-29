+++
title = "Props"
chapter = true
weight = 3
pre = "<b>3. </b>"
+++

# Props

Las props son las propiedades que se le pasan al componente, son como los argumentos de las funciones que estos esperan a ser manejados por la misma.

Podemos enviar una prop al componente de la siguiente manera:

En el archivo principal a nuestro componente **ComponentUser** le vamos a pasar 2 props, una llada **nombre** y otra **puesto**.

{{< tabs >}}
{{% tab name="main.jsx" %}}

```jsx
<ComponentUser nombre="Ana" puesto="Frontend Developer">
```

{{% /tab %}}
{{% tab name="ComponentUser.jsx" %}}

```jsx
//El componente recibe las props nombre y puesto
const ComponentUser = ({ nombre, puesto }) => {
  return (
    <div>
      <span>
        Hola {nombre} tu puesto es: {puesto}
      </span>
    </div>
  );
};
```

{{% /tab %}}
{{< /tabs >}}

La salida seria algo así:

```bash
Hola Ana tu puestos es: Frontend Developer
```

# PropTypes

Es una característica de la biblioteca de React que se utiliza para verificar/establecer el tipo de una propiedad (prop) en un componente.

##### Instalación de PropTypes

En la raíz de nuestro proyecto corremos el siguiente comando en la terminal.

```bash
npm install prop-types
```

Para poder utilizar esta caracteristica debemos importarla al inicio del docuemnto en el cual vamos a utilizarlo.

```jsx
import PropTypes from "prop-types";
```

Para establecer una propiedad se deben crear un objeto de tipo **propTypes** (prop - valor) enlazando al componente.

> La porp va seguida de la palabra **propTypes**.< tipo >.< si es requerido el valor >

- en el valor se puede establecer el **tipo de dato** de esa propiedad, si es un **string, number, boolean**, etc...

- como parametro opcional se puede establecer si dicha propiedad es requerida o no con la key **.isRequired**

Ejemplo:

```jsx
Componente.propTypes = {
  clave: propTypes.tipoDato.isRequired, //ejemplo
};
```

A continuación al componente **UserComponent** se le establecen las caracteristicas de la prop **nombre** y **edad**.

```jsx
UserComponente.propTypes = {
  nombre: PropTypes.string.isRequired,
  edad: PropTypes.number.isRequired,
};
```

Un ejemplo practico:

> archivo **main.jsx**

```jsx
import React from "react";
import ReactDOM from "react-dom/client";
import UserComponent from "./UserComponent";
import "./style.css";

ReactDOM.createRoot(document.getElementById("root")).render(
  <React.StrictMode>
    <UserComponent nombre="Luis" />
  </React.StrictMode>
);
```

> archivo del componente **UserComponent.jsx**

```jsx
//importacion de la libreria
import PropTypes from "prop-types";

const UserComponent = ({ nombre }) => {
  return <h1>Bienvenido {nombre}</h1>;
};
export default UserComponent;

//PropTypes
UserComponent.propTypes = {
  nombre: PropTypes.string.isRequired,
};
```
